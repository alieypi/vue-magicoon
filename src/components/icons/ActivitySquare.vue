<script setup>
defineProps({
  type: {
    type: String,
    default: "Regular",
  },
  size: {
    type: [String, Number],
    default: 24,
  },
  color: {
    type: String,
    default: "#000",
  },
});
</script>

<template>
  <svg v-if="type === 'Light'" :width="size" :height="size" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
    <path
      :fill="color"
      d="M17.625,2.5H6.375C3.84,2.5,2.5,3.84,2.5,6.375v11.25C2.5,20.16,3.84,21.5,6.375,21.5h11.25c2.535,0,3.875-1.34,3.875-3.875V6.375C21.5,3.84,20.16,2.5,17.625,2.5ZM20.5,17.625c0,1.961-.914,2.875-2.875,2.875H6.375c-1.961,0-2.875-.914-2.875-2.875V6.375C3.5,4.414,4.414,3.5,6.375,3.5h11.25c1.961,0,2.875.914,2.875,2.875ZM17.354,9.646a.5.5,0,0,1,0,.708L14.56,13.147a1.5,1.5,0,0,1-2.12,0l-1.589-1.585a.5.5,0,0,0-.707,0l-2.79,2.791a.5.5,0,0,1-.708-.708l2.791-2.79a1.5,1.5,0,0,1,2.121,0l1.588,1.585a.5.5,0,0,0,.707,0l2.793-2.794A.5.5,0,0,1,17.354,9.646Z"
    />
  </svg>
  <svg v-else-if="type === 'Regular'" :width="size" :height="size" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
    <path
      :fill="color"
      d="M17.625,21.75H6.375c-2.66,0-4.125-1.465-4.125-4.125V6.375c0-2.66,1.465-4.125,4.125-4.125h11.25c2.66,0,4.125,1.465,4.125,4.125v11.25C21.75,20.285,20.285,21.75,17.625,21.75Zm-11.25-18c-1.84,0-2.625.785-2.625,2.625v11.25c0,1.84.785,2.625,2.625,2.625h11.25c1.84,0,2.625-.785,2.625-2.625V6.375c0-1.84-.785-2.625-2.625-2.625ZM7.53,14.53l2.791-2.79a.249.249,0,0,1,.353,0l1.589,1.585a1.752,1.752,0,0,0,2.474,0L17.53,10.53a.75.75,0,0,0-1.06-1.06l-2.794,2.793a.25.25,0,0,1-.353,0l-1.589-1.586a1.753,1.753,0,0,0-2.474,0L6.47,13.47a.75.75,0,1,0,1.06,1.06Z"
    />
  </svg>
  <svg v-else-if="type === 'Filled'" :width="size" :height="size" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
    <path
      :fill="color"
      d="M17.625,3H6.375Q3,3,3,6.375v11.25Q3,21,6.375,21h11.25Q21,21,21,17.625V6.375Q21,3,17.625,3Zm-.095,7.53-2.793,2.794a1.752,1.752,0,0,1-2.474,0L10.674,11.74a.249.249,0,0,0-.353,0L7.53,14.53a.75.75,0,0,1-1.06-1.06l2.79-2.791a1.753,1.753,0,0,1,2.474,0l1.589,1.586a.25.25,0,0,0,.353,0L16.47,9.47a.75.75,0,0,1,1.06,1.06Z"
    />
  </svg>

  <svg v-else-if="type === 'Duotone'" :width="size" :height="size" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
    <g>
      <path :fill="color" opacity=".3" d="M3,17.625V6.375Q3,3,6.375,3h11.25Q21,3,21,6.375v11.25Q21,21,17.625,21H6.375Q3,21,3,17.625Z" />
      <path
        :fill="color"
        d="M7,14.75a.75.75,0,0,1-.53-1.28l2.79-2.791a1.753,1.753,0,0,1,2.474,0l1.589,1.586a.25.25,0,0,0,.353,0L16.47,9.47a.75.75,0,0,1,1.06,1.06l-2.793,2.794a1.752,1.752,0,0,1-2.474,0L10.674,11.74a.249.249,0,0,0-.353,0L7.53,14.53A.744.744,0,0,1,7,14.75Z"
      />
    </g>
  </svg>
</template>
