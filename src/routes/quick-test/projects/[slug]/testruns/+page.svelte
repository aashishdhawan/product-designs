<script>
    import Fullnavbar from '$lib/quick-test/fullnavbar.svelte';
    import ProjectHeader from '../../header.svelte';
</script>
<Fullnavbar/>
<ProjectHeader selection="Test Runs"/>
<!-- 3 column wrapper -->
<div class="mx-auto w-full grow lg:flex">
    <!-- Left sidebar & main wrapper -->
    <div class="flex-1 xl:flex">
      <div class="xl:flex-1">
        <!-- Main area -->
        <div class="flow-root">
    <div class="-my-2 overflow-x-auto ">
      <div class="inline-block min-w-full py-3 align-middle sm:px-6 lg:px-8">    
    
        <div class="overflow-hidden ">
          <table class="min-w-full divide-y divide-gray-300">
            <tbody class="divide-y divide-gray-200 bg-white ml-4">
                <tr>
                    <td class="whitespace-nowrap py-3 pl-4 pr-3 text-sm font-medium text-gray-900 sm:pl-0 w-full hover:underline cursor-pointer">
                      <a href="/quick-test/projects/1/testruns/1"><span>Smoke Testing</span>
                        <div class="mt-1 flex items-center gap-x-2 text-xs leading-5 text-gray-500 font-normal">
                            <p class="whitespace-nowrap">Started on Jan 12, 2023</p>
                            <svg viewBox="0 0 2 2" class="h-0.5 w-0.5 fill-current">
                                <circle cx="1" cy="1" r="1" />
                              </svg>

                                <p class="whitespace-nowrap">Due on Jan 12, 2023</p>
                                <svg viewBox="0 0 2 2" class="h-0.5 w-0.5 fill-current">
                                  <circle cx="1" cy="1" r="1" />
                                </svg>
                                <p class="whitespace-nowrap">100 test cases</p>
  
                              </div>
                            </a> 
        </td>
                    <td class="whitespace-nowrap px-3 py-3 text-sm text-gray-500">
                        <span class="inline-flex items-center rounded-md bg-yellow-50 px-2 py-1 text-xs font-medium text-yellow-700 ring-1 ring-inset ring-yellow-600/20"> In Progress</span>
                      </td>
                            <td class="relative whitespace-nowrap py-3 pl-3 pr-4 text-right text-sm font-medium sm:pr-0">
                    </td>
                    <td><div class="flex justify-end text-center items-center gap-2 text-xs"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-cy="test-run-0-edit" class="text-indigo-500 h-4 w-4 cursor-pointer"><path d="M17.414 2.586a2 2 0 00-2.828 0L7 10.172V13h2.828l7.586-7.586a2 2 0 000-2.828z"></path><path fill-rule="evenodd" d="M2 6a2 2 0 012-2h4a1 1 0 010 2H4v10h10v-4a1 1 0 112 0v4a2 2 0 01-2 2H4a2 2 0 01-2-2V6z" clip-rule="evenodd"></path></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-cy="test-run-0-delete" class="text-red-400 h-4 w-4 cursor-pointer"><path fill-rule="evenodd" d="M9 2a1 1 0 00-.894.553L7.382 4H4a1 1 0 000 2v10a2 2 0 002 2h8a2 2 0 002-2V6a1 1 0 100-2h-3.382l-.724-1.447A1 1 0 0011 2H9zM7 8a1 1 0 012 0v6a1 1 0 11-2 0V8zm5-1a1 1 0 00-1 1v6a1 1 0 102 0V8a1 1 0 00-1-1z" clip-rule="evenodd"></path></svg></div></td>

                  </tr>
                {#each Array(5) as _, index (index)}
                <tr>
                    <td class="whitespace-nowrap py-3 pl-4 pr-3 text-sm font-medium text-gray-900 sm:pl-0 w-full hover:underline cursor-pointer">
                      <a href="/quick-test/projects/1/testruns/1">Regression Testing {index + 2}
                      <div class="mt-1 flex items-center gap-x-2 text-xs leading-5 text-gray-500 font-normal">
                        <p class="whitespace-nowrap">Completed on Jan 12, 2023 by Aashish Dhawan</p>
                        <svg viewBox="0 0 2 2" class="h-0.5 w-0.5 fill-current">
                          <circle cx="1" cy="1" r="1" />
                        </svg>
                        <p class="whitespace-nowrap">80 Passed, 20 Failed, 9 Blocked</p>
                                          </div>
                                        </a> 
                </td>
                    <td class="whitespace-nowrap px-3 py-3 text-sm text-gray-500">
                        <span class="inline-flex items-center rounded-md bg-green-50 px-2 py-1 text-xs font-medium text-green-700 ring-1 ring-inset ring-green-600/20">Completed</span>
                      </td>
                            <td class="relative whitespace-nowrap py-3 pl-3 pr-4 text-right text-sm font-medium sm:pr-0">
                    </td>
                    <td><div class="flex justify-end text-center items-center gap-2 text-xs"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-cy="test-run-0-edit" class="text-indigo-500 h-4 w-4 cursor-pointer"><path d="M17.414 2.586a2 2 0 00-2.828 0L7 10.172V13h2.828l7.586-7.586a2 2 0 000-2.828z"></path><path fill-rule="evenodd" d="M2 6a2 2 0 012-2h4a1 1 0 010 2H4v10h10v-4a1 1 0 112 0v4a2 2 0 01-2 2H4a2 2 0 01-2-2V6z" clip-rule="evenodd"></path></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-cy="test-run-0-delete" class="text-red-400 h-4 w-4 cursor-pointer"><path fill-rule="evenodd" d="M9 2a1 1 0 00-.894.553L7.382 4H4a1 1 0 000 2v10a2 2 0 002 2h8a2 2 0 002-2V6a1 1 0 100-2h-3.382l-.724-1.447A1 1 0 0011 2H9zM7 8a1 1 0 012 0v6a1 1 0 11-2 0V8zm5-1a1 1 0 00-1 1v6a1 1 0 102 0V8a1 1 0 00-1-1z" clip-rule="evenodd"></path></svg></div></td>
                  </tr>
                {/each}
  
              <!-- More people... -->
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
      </div>
    </div>
  
    <div class="shrink-0 border-t border-gray-200 px-4 py-6 sm:px-6 lg:w-96 lg:border-l lg:border-t-0 lg:pr-8 xl:pr-6 h-screen">
      <!-- Right column area -->
        
          <h3 class="text-base font-semibold leading-6 text-gray-900">Test Runs</h3>
          <div class="mt-2 max-w-xl text-sm text-gray-500">
            <p>Test run is a collection of test cases which are tested to create a report about passing and failing tests. </p>
          </div>
          <div class="mt-5">
            <button type="button" class="inline-flex items-center rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-500">Start Another Test Run</button>
          </div>
    </div>
  </div>