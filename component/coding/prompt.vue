<template>
	<div class="container w-full">
		<div class="w-full">
			<p class="my-2 text-center text-3xl font-semibold">ChatGPTプロンプト生成</p>
		</div>
		<div class="w-full my-4">
			<p class="text-center">※以下のチェックボックスの順番は画面上から変更出来ません</p>
			<table class="w-6/12 px-2 text-center mx-auto">
				<tr>
					<td class="w-4/12 text-left">
						<label><input type="checkbox" class="h-5 w-5" v-model="qaSwitch" /><span class="ml-2">質問内容</span></label>
					</td>
					<td class="w-4/12 text-left">
						<label><input type="checkbox" class="h-5 w-5" v-model="errorSwitch" /><span class="ml-2">エラー文</span></label>
					</td>
					<td class="w-4/12 text-left">
						<label><input type="checkbox" class="h-5 w-5" v-model="envSwitch" /><span class="ml-2">環境</span></label>
					</td>
				</tr>
				<tr>
					<td class="w-4/12 text-left">
						<label><input type="checkbox" class="h-5 w-5" v-model="codeSwitch" /><span class="ml-2">ソースコード</span></label>
					</td>
					<td class="w-4/12 text-left">
						<label><input type="checkbox" class="h-5 w-5" /><span class="ml-2"></span></label>
					</td>
					<td class="w-4/12 text-left">
						<label><input type="checkbox" class="h-5 w-5" /><span class="ml-2"></span></label>
					</td>
				</tr>
				<tr>
					<td class="w-4/12 text-left">
						<label><input type="checkbox" class="h-5 w-5" /><span class="ml-2"></span></label>
					</td>
					<td class="w-4/12 text-left">
						<label><input type="checkbox" class="h-5 w-5" /><span class="ml-2"></span></label>
					</td>
					<td class="w-4/12 text-left">
						<label><input type="checkbox" class="h-5 w-5" /><span class="ml-2"></span></label>
					</td>
				</tr>
			</table>
		</div>
		<div class="flex">
			<div class="w-1/2 px-2 text-left border-r-2 h-screen">
				<div class="flex">
					<div class="w-2/12 h-10 text-center bg-gray-500 hover:bg-gray-700 hover:cursor-potinter text-white font-bold mr-2 py-1 rounded" @click="resetForm">
						<span class="mdi mdi-refresh text-2xl"></span>
					</div>
					<div class="w-10/12 h-10 text-center bg-blue-500 text-white font-bold py-2 px-2 rounded">
						<span>入力フォーム</span>
					</div>
				</div>
				<form ref="myForm">
					<div class="mt-2">
						<div v-if="qaSwitch">
							<label class="block leading-6 text-gray-900">質問内容</label>
							<div class="mt-2">
								<input v-model="qa" class="block w-full rounded-md p-1.5 text-gray-900 shadow-sm ring-1 ring-gray-300" />
							</div>
						</div>
						<div class="mt-2" v-if="envSwitch">
							<div class="flex items-center justify-between">
								<label for="password" class="block leading-6 text-gray-900">環境</label>
							</div>
							<div class="mt-2">
								<input v-model="env" class="block w-full rounded-md p-1.5 text-gray-900 shadow-sm ring-1 ring-gray-300" />
							</div>
						</div>
						<div class="mt-2" v-if="errorSwitch">
							<div class="flex items-center justify-between">
								<label for="password" class="block leading-6 text-gray-900">エラー文</label>
							</div>
							<div class="mt-2">
								<textarea
									v-model="errorContext"
									id="error-context"
									wrap="hard"
									@input="adjustTextareaHeight"
									class="block w-full rounded-md p-1.5 text-gray-900 shadow-sm ring-1 ring-gray-300 resize-none"
								></textarea>
							</div>
						</div>
						<div class="mt-2" v-if="codeSwitch">
							<div class="flex items-center justify-between">
								<label for="password" class="block leading-6 text-gray-900">ソースコード（エスケープさせる処理めんどくさいの改行無し）</label>
							</div>
							<div class="mt-2">
								<textarea
									v-model="codeContext"
									id="code-context"
									wrap="hard"
									@input="adjustCodeareaHeight"
									class="block w-full rounded-md p-1.5 text-gray-900 shadow-sm ring-1 ring-gray-300 resize-none"
								></textarea>
							</div>
						</div>
					</div>
				</form>
			</div>
			<div class="w-1/2 px-2 text-left border-r-2 h-screen">
				<button v-if="condition === 'copybutton'" @click="copyToClipboard" class="h-10 w-full text-center bg-gray-500 hover:bg-gray-700 transition text-white font-bold p-2 rounded">
					<span>クリップボードにコピーする<span class="mdi mdi-clipboard-text-outline m-0 p-0 ml-1"></span></span>
				</button>
				<v-alert v-if="condition === 'success'" class="h-10 text-white p-2 font-semibold mb-0" type="success">コピーに成功しました</v-alert>
				<v-alert v-if="condition === 'error'" class="h-10 text-white p-2 font-semibold mb-0" type="error">コピーに失敗しました</v-alert>

				<div id="contextForChatgpt" ref="contextForChatgpt" class="mt-2 p-2 bg-gray-200 rounded-md h-full">
					<div v-if="qaSwitch">
						<label class="mb-2" for="name">## 質問内容</label>
						<p>{{ qa }}</p>
					</div>
					<div v-if="envSwitch">
						<label class="mb-2" for="address">## 環境</label>
						<p>{{ env }}</p>
					</div>
					<div v-if="errorSwitch">
						<label class="mb-2" for="address">## エラー文</label>
						<p v-html="formattedErrorContext"></p>
					</div>
					<div v-if="codeSwitch">
						<label class="mb-2" for="address">## ソースコード</label>
						<p>{{ codeContext }}</p>
						<!-- <p v-html="formattedCodeContext"></p> -->
					</div>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
module.exports = {
	data: function () {
		return {
			name: "PromptComponent",
			qaSwitch: true,
			errorSwitch: false,
			envSwitch: false,
			codeSwitch: false,
			contextForChatgpt: "",
			condition: "copybutton", // 表示する要素を制御する条件
			qa: "",
			env: "",
			codeContext: "",
			errorContext: "",
		};
	},
	mounted() {
		// Clipboard.jsの初期化
		new Clipboard(this.$refs.copyButton);
	},
	computed: {
		formattedErrorContext() {
			// 改行文字をHTMLの改行タグに変換する
			return this.errorContext.replace(/\n/g, "<br>");
		},
		formattedCodeContext() {
			// 改行文字をHTMLの改行タグに変換する
			return this.codeContext.replace(/\n/g, "<br>");
		},
	},
	methods: {
		resetForm() {
			(this.qa = ""), (this.env = ""), (this.codeContext = ""), (this.errorContext = "");
		},
		adjustTextareaHeight(event) {
			const textarea = event.target;
			textarea.style.height = "auto";
			textarea.style.height = `${textarea.scrollHeight}px`;
		},
		adjustCodeareaHeight(event) {
			const textarea = event.target;
			textarea.style.height = "auto";
			textarea.style.height = `${textarea.scrollHeight}px`;
		},
		copyToClipboard() {
			const textToCopy = this.$refs.contextForChatgpt.innerText; // コピーしたいテキストを指定
			navigator.clipboard
				.writeText(textToCopy)
				.then(() => {
					this.condition = "success"; // v-alertを表示する
					// 3秒後にv-alertを非表示にする
					setTimeout(() => {
						this.condition = "copybutton";
					}, 2000);
				})
				.catch((error) => {
					this.condition = "error"; // v-alertを表示する
					// 3秒後にv-alertを非表示にする
					setTimeout(() => {
						this.condition = "copybutton";
					}, 2000);
				});
		},
	},
};
</script>
