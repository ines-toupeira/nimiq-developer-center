<script setup lang="ts">
const baseUrl = import.meta.env.BASE_URL

// Redirect the user to the design kit page when they right click on the logo
// unless they are already on the design kit page
const designKitUrl = `${baseUrl}build/ui/design-kit/guidelines`
function onRightClick(e: MouseEvent) {
  if (window.location.pathname === designKitUrl)
    return

  e.preventDefault()
  window.location.pathname = designKitUrl
}
</script>

<template>
  <a :href="baseUrl" flex items-center gap-x-10 @click.right="onRightClick">
    <svg h-24 flex-1 xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 102 25">
      <path
        fill="url(#a)"
        d="m26.697 11.375-5.625-9.75A2.255 2.255 0 0 0 19.122.5H7.872C7.07.5 6.327.927 5.926 1.625L.3 11.375a2.253 2.253 0 0 0 0 2.25l5.625 9.75A2.244 2.244 0 0 0 7.872 24.5h11.25c.803 0 1.545-.427 1.946-1.125l5.625-9.75a2.244 2.244 0 0 0 .004-2.25Z"
      />
      <path
        un-fill="darkblue dark:white"
        d="M46.688 5.375h2.444v14.25H47.25l-7.688-9.938v9.938h-2.437V5.375H39l7.688 9.938V5.374ZM54 19.75V5.5h2.625v14.25H54ZM73.313 5.813h2.062v14.25h-2.25V11.25l-3.844 8.813h-1.687L63.75 11.25v8.813H61.5V5.813h2.063l4.874 11.156 4.876-11.157ZM80.25 20.063V5.813h2.625v14.25H80.25ZM100.41 16.815c-.765 1.519-1.954 2.411-3.007 2.846.123.285.704 1.08 1.143 1.538.439.457.9.922 1.485 1.395L98.25 24c-.656-.457-1.226-1.005-1.808-1.642a11.937 11.937 0 0 1-1.526-2.127 11.98 11.98 0 0 1-.603.019c-1.452 0-2.663-.296-3.71-.885-1.045-.592-1.844-1.44-2.395-2.55-.507-1.009-.833-2.355-.833-3.878 0-1.522.281-2.767.84-3.877.559-1.106 1.361-1.958 2.407-2.55 1.047-.592 2.27-.885 3.69-.885 1.422 0 2.663.296 3.71.885 1.045.593 1.844 1.44 2.396 2.55.555 1.11.832 2.355.832 3.877 0 1.523-.334 2.873-.84 3.878Zm-9.274.011c.758.908 1.815 1.361 3.177 1.361 1.36 0 2.422-.453 3.176-1.36.757-.912 1.136-2.195 1.136-3.89 0-1.683-.379-2.996-1.136-3.896-.758-.9-1.815-1.354-3.177-1.354-1.36 0-2.422.447-3.176 1.343C90.38 9.926 90 11.243 90 12.938c0 1.694.379 2.977 1.136 3.888Z"
      />
      <defs>
        <radialGradient
          id="a" cx="0" cy="0" r="1" gradientTransform="matrix(-26.9977 0 0 -24 26.998 24.5)"
          gradientUnits="userSpaceOnUse"
        >
          <stop stop-color="#EC991C" />
          <stop offset="1" stop-color="#E9B213" />
        </radialGradient>
      </defs>
    </svg>
    <span max-lg:hidden md:text-20>Developer Center</span>
  </a>
</template>
  }
