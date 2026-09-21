<template>
  <a
    href="#"
    target="blank"
    rel="noopener noreferrer"
    class="shadow- transition:all flex w-full items-center gap-4 rounded-xl border border-gray-700 bg-gray-800 p-4 shadow-gray-900/50 duration-300 hover:scale-[1.02] hover:border-green-600 hover:shadow-xl hover:shadow-green-500/20"
  >
    <!-- Icon Container -->
    <div
      class="flex h-12 w-12 shrink-0 items-center justify-center rounded-lg bg-gray-700 text-green-400"
    >
      <svg
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentcolor"
        class="h-6 w-6"
      >
        <path
          stroke-lincap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M6 12v9a1 1 0 0 1-2 0V4c0-1.1.9-2 2-2h6c1.1 0 1.999.9 1.999 2H18a2 2 0 0 1 2 2v6a2 2 0 0 1-2 2h-5a2 2 0 0 1-1.997-2zm0-8v6h7v2h5.002V6H12V4z"
        />
      </svg>
    </div>

    <!-- Text Content -->
    <div class="min-w-0 flex-1">
      <h3 class="truncate font-display font-semibold text-white">Link Title</h3>
      <p class="truncate text-sm text-gray-400">
        Lorem ipsum dolor sit amet consectetur adipisicing elit.
      </p>
    </div>
  </a>
</template>
