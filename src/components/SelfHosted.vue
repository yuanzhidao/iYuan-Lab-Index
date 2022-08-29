<script setup>
import Banner from "./Banner.vue";
</script>

<template>
	<h2 class="dark:text-slate-300 m-6 text-gray-500 text-2xl -mb-1 font-bold">Self-Hosted Services</h2>

	<Banner />

	<div class="grid grid-cols-1 lg:grid-cols-2">
		<a rel="noopener noreferrer" class="m-6 cursor-not-allowed">
			<div class="dark:shadow p-10 rounded-3xl bg-gradient-to-br from-blue-400 to-blue-500 dark:from-blue-400/80 dark:to-blue-500/80 shadow-2xl shadow-blue-500/50 hover:scale-[102%] transition duration-500">
				<div class="flex flex-col items-start text-white dark:text-gray-200">
					<div class="w-16 h-16 mb-3">
						<img src="/static/img/matomo.svg" alt="Matomo Logo" class="w-16 h-16" />
					</div>
					<h2 class="mb-3 font-bold text-3xl md:text-5xl">Matomo</h2>
					<p class="text-base leading-relaxed md:text-lg">开源 Analytics 统计分析软件</p>
					<div class="hidden lg:flex justify-center items-center w-full">
						<img style="height: 23.5rem" src="/static/img/analytics.svg" alt="Analytics" class="scale-[160%]" />
					</div>
				</div>
			</div>
		</a>

		<div class="-mb-6">
			<a class="cursor-not-allowed m-6">
				<div class="dark:shadow mx-6 p-10 rounded-3xl bg-gradient-to-br from-yellow-400 to-red-400 dark:from-yellow-400/80 dark:to-red-400/80 shadow-2xl shadow-yellow-300/50 hover:scale-[102%] transition duration-500">
					<div class="flex flex-col items-start text-white dark:text-gray-200">
						<div class="w-16 h-16 mb-3">
							<img src="/static/img/blessing.png" alt="Minecraft Golden Chestplate" class="w-16 h-16" />
						</div>
						<h2 class="mb-3 font-bold text-3xl md:text-5xl">Blessing Skin</h2>
						<p class="text-base leading-relaxed md:text-lg">Blessing Skin 是一款能让您上传、管理和分享您的 Minecraft 皮肤和披风的 Web 应用程序。</p>
					</div>
				</div>
			</a>

			<a rel="noopener noreferrer" class="m-6 cursor-not-allowed">
				<div class="dark:shadow m-6 p-10 rounded-3xl bg-gradient-to-br from-sky-400 to-sky-500 dark:from-sky-400/80 dark:to-sky-500/80 shadow-2xl shadow-sky-500/50 hover:scale-[102%] transition duration-500">
					<div class="flex flex-col items-start text-white dark:text-gray-200">
						<div class="w-16 h-16 mb-3">
							<img src="/static/img/cloudreve.png" alt="Cloudreve Logo" class="w-16 h-16" />
						</div>
						<h2 class="mb-3 font-bold text-3xl md:text-5xl">Cloudreve</h2>
						<p class="text-base leading-relaxed md:text-lg">Cloudreve 可助你即刻构建出兼备自用或公用的网盘服务，通过多种存储策略的支持、虚拟文件系统等特性实现灵活的文件管理体验。</p>
					</div>
				</div>
			</a>
		</div>

		<a class="m-6 col-span-full cursor-not-allowed">
			<div class="dark:shadow p-10 rounded-3xl bg-gradient-to-br from-pink-400 to-pink-500 dark:from-pink-400/80 dark:to-pink-500/80 shadow-2xl shadow-pink-400/50 hover:scale-[102%] transition duration-500">
				<div class="flex flex-col items-start text-white dark:text-gray-200">
					<div class="w-16 h-16 mb-3">
						<img src="/static/img/bitwarden.png" alt="Bitwarden Logo" class="w-16 h-16" />
					</div>
					<h2 class="mb-3 font-bold text-3xl md:text-5xl">Bitwarden</h2>
					<p class="text-base leading-relaxed md:text-lg">适用于个人、团队和商业组织的密码管理开源解决方案。</p>
				</div>
			</div>
		</a>

		<a href="https://alist.ezh.ink/" target="_blank" rel="noreferrer noopener" class="m-6 col-span-full">
			<div class="dark:shadow p-10 rounded-3xl bg-gradient-to-br from-indigo-400 to-indigo-500 dark:from-indigo-400/80 dark:to-indigo-500/80 shadow-2xl shadow-indigo-400/50 hover:scale-[102%] transition duration-500">
				<div class="flex flex-col items-start text-white dark:text-gray-200">
					<div class="w-16 h-16 mb-3 rounded-full overflow-hidden">
						<img src="/static/img/alist.svg" alt="Alist Logo" class="w-16 h-16" />
					</div>
					<h2 class="mb-3 font-bold text-3xl md:text-5xl">Alist</h2>
					<p class="text-base leading-relaxed md:text-lg">一款支持多种存储的目录文件列表程序，支持 Web 浏览与 Webdav，后端基于 Gin，前端使用 React。</p>
				</div>
			</div>
		</a>
	</div>
</template>
