<script>
	let login = [
		{ title: 'Login', link: '/quick-release/login' },
		{ title: 'Forgot Password', link: '/quick-release/forgot-password' },
		{ title: 'Reset Password', link: '/quick-release/reset-password' }
	];

	let signup = [
		{ title: 'Signup', link: '/quick-release/signup' },
		{ title: 'Create Team', link: '/quick-release/signup/team' }
	];

	let changelog = [
		{ title: 'Admin Changelogs', link: '/quick-release/changelog' },
		{ title: 'Empty State', link: '/quick-release/changelog/empty' },
		{ title: 'Add Change Log', link: '/quick-release/changelog/new' },
		{ title: 'Public Changelog Detail', link: '/quick-release/changelog/1' },
		{ title: 'Public Changelog list', link: '/quick-release/changelog/public' },
		{ title: 'Settigns - General', link: '/quick-release/settings/team/general' },
		{ title: 'Settings - tags', link: '/quick-release/settings/team/tags' }
	];

	let profile = [
		{ title: 'General', link: '/quick-release/settings/profile/general' },
		{ title: 'Change Password', link: '/quick-release/settings/profile/password' },
		{ title: 'Preferences', link: '/quick-release/settings/profile/preferences' }
	];

	let account = [];

	let team = [];

	let workflows = [
		{ title: 'Login', screens: login },
		{ title: 'Signup', screens: signup },
		{ title: 'Changelog', screens: changelog },
		{ title: 'Profile Settings', screens: profile }
	];

	let workflows2 = [
		{ title: 'Account Settings', screens: account },
		{ title: 'Team Settings', screens: team }
	];
</script>

<!-- 3 column wrapper -->
<div class="mx-auto w-full flex-grow lg:flex">
	<!-- Left sidebar & main wrapper -->
	<div class="min-w-0 flex-1 bg-white xl:flex">
		<div
			class="border-b border-gray-200 bg-white xl:w-64 xl:flex-shrink-0 xl:border-b-0 xl:border-r xl:border-gray-200">
			<div class="h-full sm:pl-6 lg:pl-8 xl:pl-0">
				<!-- Start left column area -->
				<div class="relative">
					{#each workflows as workflow}
						<div
							class="sticky top-0 z-10 border-t border-b border-gray-200 bg-gray-50 px-6 py-1 text-sm font-medium text-gray-500">
							<h3>{workflow.title}</h3>
						</div>
						<ul role="list" class="relative z-0 divide-y divide-gray-200">
							{#each workflow.screens as screen}
								<li class="bg-white">
									<div
										class="relative flex items-center space-x-3 px-6 py-2 focus-within:ring-2 focus-within:ring-inset
								focus-within:ring-indigo-500 hover:bg-gray-50">
										<div class="min-w-0 flex-1">
											<a href={screen.link} class="focus:outline-none">
												<p class="text-sm font-medium text-gray-900">{screen.title}</p>
											</a>
										</div>
									</div>
								</li>
							{/each}
						</ul>
					{/each}
				</div>
				<!-- End left column area -->
			</div>
		</div>

		<div
			class="border-b border-gray-200 bg-white xl:w-64 xl:flex-shrink-0 xl:border-b-0 xl:border-r xl:border-gray-200">
			<div class="h-full sm:pl-6 lg:pl-8 xl:pl-0">
				<!-- Start left column area -->
				<div class="relative">
					{#each workflows2 as workflow}
						<div
							class="sticky top-0 z-10 border-t border-b border-gray-200 bg-gray-50 px-6 py-1 text-sm font-medium text-gray-500">
							<h3>{workflow.title}</h3>
						</div>
						<ul role="list" class="relative z-0 divide-y divide-gray-200">
							{#each workflow.screens as screen}
								<li class="bg-white">
									<div
										class="relative flex items-center space-x-3 px-6 py-2 focus-within:ring-2 focus-within:ring-inset
							focus-within:ring-indigo-500 hover:bg-gray-50">
										<div class="min-w-0 flex-1">
											<a href={screen.link} class="focus:outline-none">
												<p class="text-sm font-medium text-gray-900">{screen.title}</p>
											</a>
										</div>
									</div>
								</li>
							{/each}
						</ul>
					{/each}
				</div>
				<!-- End left column area -->
			</div>
		</div>
	</div>
</div>
