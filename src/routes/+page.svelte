<script lang="ts">
  import { ShareButton } from '$lib';

  const url = encodeURI(
    `https://social-plugins.line.me/lineit/share?url=https://twitter.com/marley_eng`
  );
</script>

<ShareButton {url} --share-button-background-color="#00b900" --share-button-hover-color="#00b900">
  <svg
    class="share-icon"
    slot="icon"
    aria-label="LINE"
    viewBox="0 0 512 512"
    xmlns="http://www.w3.org/2000/svg"
  >
    <path
      d="M512.017 227.437c-2.734 61.513-28.706 103.889-69.715 140.796-72.448 64.247-187.272 143.53-202.308 131.227-15.037-19.137 28.706-64.246-27.34-71.08C92.365 411.975.778 327.224.778 227.436c0-112.09 116.191-205.042 256.987-205.042 140.796 0 258.354 92.953 254.253 205.042z"
      fill="#fff"
      style="stroke-width:1.36695"
      transform="translate(0 -5.565)"
    /><path
      d="M413.596 223.24H367.12m46.476-49.21h-49.21v98.42h49.21m-168.135 0v-98.42l73.816 98.42v-98.42m-121.659 98.42v-98.42m-90.218 0v98.42h50.577"
      fill="none"
      stroke="#00b900"
      stroke-linecap="round"
      stroke-linejoin="round"
      stroke-width="24.25"
    />
  </svg>

  <span class="share-text"> 送る </span>
</ShareButton>

<style>
  .share-icon {
    width: 2em;
    height: 2em;
  }

  .share-text {
    font-size: 1.3em;
    font-weight: 600;
  }
</style>
