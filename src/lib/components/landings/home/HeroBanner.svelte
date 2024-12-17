<script lang="ts">
  import '$lib/components/mariui/blocks/buttons/raised.css'
  interface landingSimpleConfigInterface {
    heroTitle: string;
    description?: string;
    buttonText?: string;
  }

  let {
    heroTitle = 'Hero Title',
    description = 'Description',
    buttonText = 'Click Me'
  }: landingSimpleConfigInterface = $props();
</script>

<section
  style="
    background-color: var(--primary-20);
  ">
  <div
    style=
    "
      padding: var(--pixel-large) var(--pixel-extra-large);

      display: flex;
      flex-direction: column;
      align-items: center;
    ">
    <h1 style=
      "
        font-size: var(--font-headline-size);
      ">{heroTitle}</h1>
    <p>{description}</p>
    <button raised-button mari-primary>Click Me</button>
  </div>
</section>
