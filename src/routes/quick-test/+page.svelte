<script>
	let settings = [{ title: 'My Profile', link: '/quick-test/settings/profile' },
	{ title: 'Change password', link: '/quick-test/settings/password' }];

	let projects = [{ title: 'Projects Home', link: '/quick-test/projects' },
	{ title: 'Milestones', link: '/quick-test/projects/1/milestones' },
	{ title: 'Milestone Detail', link: '/quick-test/projects/1/milestones/1' },
	{ title: 'Test Runs', link: '/quick-test/projects/1/testruns' },
	{ title: 'Test Runs Detail', link: '/quick-test/projects/1/testruns/1' }
];


	let dashboard = [		
	];

	let workflows = [
		{ title: 'Settings', screens: settings },
		{ title: 'Projects', screens: projects },
		{ title: 'Dashboard', screens: dashboard }
	];
</script>
<!-- 3 column wrapper -->
<div class="mx-auto w-full flex-grow lg:flex">
	<!-- Left sidebar & main wrapper -->
	<div class="min-w-0 flex-1 bg-white xl:flex">
		<div class="border-b border-gray-200 bg-white xl:w-64 xl:flex-shrink-0 xl:border-b-0 xl:border-r xl:border-gray-200">
			<div class="h-full sm:pl-6 lg:pl-8 xl:pl-0">
				<!-- Start left column area -->
				<div class="relative"> {#each workflows as workflow} <div
																																																																																																																																																											class="sticky top-0 z-10 border-t border-b border-gray-200 bg-gray-50 px-6 py-1 text-sm font-medium text-gray-500">
						<h3>{workflow.title}</h3>
					</div>
					<ul role="list" class="relative z-0 divide-y divide-gray-200"> {#each workflow.screens as screen} <li class="bg-white">
							<div class="relative flex items-center space-x-3 px-6 py-2 focus-within:ring-2 focus-within:ring-inset
								focus-within:ring-indigo-500 hover:bg-gray-50">
								<div class="min-w-0 flex-1">
									<a href={screen.link} class="focus:outline-none">
										<p class="text-sm font-medium text-gray-900">{screen.title}</p>
									</a>
								</div>
							</div>
						</li> {/each} </ul> {/each}
				</div>
				<!-- End left column area -->
			</div>
		</div>
	</div>
</div>