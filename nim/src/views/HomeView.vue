<script setup>
import { onMounted } from 'vue'
import { supabase } from '../lib/supabase'

onMounted(async () => {
  const { data, error } = await supabase
    .from('test')
    .select('*')

  console.log(data, error)
})
</script>

<template>
  <main>
    <TheWelcome />
  </main>
</template>
