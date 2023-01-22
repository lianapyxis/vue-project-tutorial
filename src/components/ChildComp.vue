<script setup>
const props = defineProps({
  msg: String
})

// declare emitted events
const emit = defineEmits(['response'])

// emit with argument
emit('response', 'hello from child')

</script>