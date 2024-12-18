<script lang="ts">
  interface tabBarInterface {
    tabsDescription: { heading: string; content: any; }[];
  }

  let {
    tabsDescription = [ {
      heading: "Nice",
      content: "<h1>lorem ipsum</h1>"
    },
    {
      heading: "Nice",
      content: "lorem ipsum"
    }],
  }: tabBarInterface = $props();

  let activeTab = $state(0);

  const handleTabClick = (index: number) => {
    activeTab = index;
  };
</script>

<main>
  <div class="tabContainer">
    <div class="tabHeader">
      {#each tabsDescription as tab, index}
        <button
          class="tabBtn {index === activeTab ? 'active' : ''}"
          onclick={() => handleTabClick(index)}
        >
          {tab.heading}</button
        >
      {/each}
    </div>

    <div class="tabContent">
      {#each tabsDescription as tab, index}
        <div class="content {index === activeTab ? 'active' : ''}">
          {tab.content}
        </div>
      {/each}

    </div>
  </div>
</main>

