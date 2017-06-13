<template>
    <div :aria-live="politeness">
        {{ 
            text.length 
            ? text 
            : null 
        }}
    </div>
</template>

<script>
export default {
  name: 'announcer',
  props: {
    text: {
      type: String
    }
  },
  data: function () {
    return {
      politeness: 'polite'
    }
  }
}
</script>
