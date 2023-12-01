<script>
    export let question = "questions";
    export let answer = 'answer';
    
  let showAnswer = true;

  function toggleAnswer() {
    showAnswer = !showAnswer;
  }
</script>

<div class="bg-[#fff] mb-10 mx-2">
  <div class="flex items-center my-5">
    <div>
      <img src="/Main/cube_box.svg" alt="cube_box" class="w-8 h-8 lg:w-10 lg:h-10" />
    </div>
    <div class="text-left text-[#2c2c2c] text-700 sm:text-2xl lg:text-3xl font-semibold ml-2 lg:ml-10">
      {question}
    </div>
    <!-- Collapsible button/icon -->
    <button class="ml-auto lg:mr-2 p-2 rounded-full transition-transform transform" on:click={toggleAnswer}>
      {#if showAnswer}
        <!-- Render the downward arrow icon when the content is uncollapsed -->
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
        </svg>
      {:else}
        <!-- Render the upward arrow icon when the content is collapsed -->
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 15l7-7 7 7"></path>
        </svg>
      {/if}
    </button>
  </div>
  <!-- Collapsible content -->
  <div class="my-2">
    <div class="text-justify text-[#2c2c2c] text-700 text-sm lg:text-lg font-normal mx-10 lg:ml-20" class:collapsed={!showAnswer}>
      {answer}
    </div>
  </div>
</div>


<style>
  .collapsed {
    max-height: 0;
    opacity: 0;
    overflow: hidden;
    transform-origin: top;
    transition: max-height 0.2s ease-out, opacity 0.2s ease-out;
  }
</style>