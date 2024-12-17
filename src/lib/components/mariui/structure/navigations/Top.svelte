<script lang="ts">
  import logo from '$lib/assets/images/logo.png';

  interface navigationsTopConfigInterface {
    sectionNumber: 1 | 2| 3 ;

    heroTitle: string;
    icon?: string;
  }

  let {
    sectionNumber = 1,
    heroTitle = "Hero Title",
    icon = logo

  }: navigationsTopConfigInterface = $props()
</script>

<section
  style="
  ">
  <nav
    style="
      display: flex;
      "
  >
  <div
    style=
      "
        display: flex;
        align-items: center;
        gap: var(--pixel-extra-small);
      ">
      <img
          style="
              width: var(--font-title-size);
              height: var(--font-title-size);
            "
          src={icon}
          alt="{heroTitle}'s logo" />
      <div
        style="
          font-family: var(--font-hero);
          font-size: var(--font-subheader-size);
        ">
        {heroTitle}
      </div>
  </div>
  </nav>
</section>