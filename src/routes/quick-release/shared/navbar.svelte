<script>
	let menu = { opened: false };

	function toggle() {
		menu.opened = !menu.opened;
	}
</script>

<nav class="bg-gray-800">
	<div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8">
		<div class="relative flex h-12 items-center justify-between">
			<div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
				<!-- Mobile menu button-->
				<button
					on:click={toggle}
					type="button"
					class="inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
					aria-controls="mobile-menu"
					aria-expanded="false">
					<span class="sr-only">Open main menu</span>

					{#if !menu.opened}
						<!--
              Icon when menu is closed.
  
              Menu open: "hidden", Menu closed: "block"
            -->
						<svg
							class="block h-6 w-6"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							aria-hidden="true">
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
						</svg>
					{/if}
					<!--
              Icon when menu is open.
  
              Menu open: "block", Menu closed: "hidden"
            -->
					{#if menu.opened}
						<svg
							class="hidden h-6 w-6"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							aria-hidden="true">
							<path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
						</svg>
					{/if}
				</button>
			</div>
			<div class="flex flex-1 items-center justify-center sm:items-stretch sm:justify-start">
				<div class="flex flex-shrink-0 items-center">
					<a href="/quick-release">
						<img
							class="block h-8 w-auto lg:hidden"
							src="https://tailwindui.com/img/logos/mark.svg?color=indigo&shade=500"
							alt="Your Company" />
						<img
							class="hidden h-8 w-auto lg:block"
							src="https://tailwindui.com/img/logos/mark.svg?color=indigo&shade=500"
							alt="Your Company" />
					</a>
				</div>
				<div class="hidden sm:ml-6 sm:block">
					<div class="flex space-x-4">
						<!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
						<a
							href="#"
							class="bg-gray-900 text-white px-3 py-2 rounded-md text-sm font-medium"
							aria-current="page">Quick Release</a>
					</div>
				</div>
			</div>
			<div
				class="absolute inset-y-0 right-0 flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0">
				<!-- Profile dropdown -->
				<div class="relative ml-3">
					<div>
						<button
							on:click={toggle}
							type="button"
							class="flex rounded-full bg-gray-800 text-sm focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-gray-800"
							id="user-menu-button"
							aria-expanded="false"
							aria-haspopup="true">
							<span class="sr-only">Open user menu</span>
							<img
								class="h-8 w-8 rounded-full"
								src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
								alt="" />
						</button>
					</div>

					<!--
              Dropdown menu, show/hide based on menu state.
  
              Entering: "transition ease-out duration-100"
                From: "transform opacity-0 scale-95"
                To: "transform opacity-100 scale-100"
              Leaving: "transition ease-in duration-75"
                From: "transform opacity-100 scale-100"
                To: "transform opacity-0 scale-95"
            -->
					{#if menu.opened}
						<div
							class="absolute right-0 z-10 mt-2 w-48 origin-top-right rounded-md bg-white py-1 shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none divide-y divide-gray-100"
							role="menu"
							aria-orientation="vertical"
							aria-labelledby="user-menu-button"
							tabindex="-1">
							<div class="px-4 py-3 text-sm text-gray-900 dark:text-white">
								<div>Bonnie Green</div>
								<div class="font-medium truncate">name@flowbite.com</div>
							</div>

							<ul
								class="py-2 text-sm text-gray-700 dark:text-gray-200"
								aria-labelledby="dropdownInformationButton">
								<li>
									<a
										href="#"
										class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
										>Quick Teams</a>
								</li>
								<li>
									<a
										href="#"
										class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
										>Quick Survey</a>
								</li>
								<li>
									<a
										href="#"
										class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
										>Quick Connect</a>
								</li>
							</ul>

							<ul
								class="py-2 text-sm text-gray-700 dark:text-gray-200"
								aria-labelledby="dropdownInformationButton">
								<li>
									<a
										href="#"
										class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
										>Account Settings</a>
								</li>
								<li>
									<a
										href="#"
										class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
										>Profile Settings</a>
								</li>
								<li>
									<a
										href="#"
										class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
										>Team Settings</a>
								</li>
							</ul>
							<div class="py-2">
								<a
									href="/quick-release/login"
									class="block px-4 py-2 text-sm text-gray-700 border-top hover:bg-gray-100 dark:hover:bg-gray-600 dark:text-gray-200 dark:hover:text-white"
									>Sign out</a>
							</div>
						</div>
					{/if}
				</div>
			</div>
		</div>
	</div>

	<!-- Mobile menu, show/hide based on menu state. -->
	<div class="sm:hidden" id="mobile-menu">
		<div class="space-y-1 px-2 pt-2 pb-3">
			<!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
			<a
				href="#"
				class="bg-gray-900 text-white block px-3 py-2 rounded-md text-base font-medium"
				aria-current="page"
				>Quick Release
			</a>
		</div>
	</div>
</nav>
