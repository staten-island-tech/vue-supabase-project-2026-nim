<script setup>
import TheWelcome from '../components/TheWelcome.vue'
import { createClient } from '@supabase/supabase-js'

const supabaseUrl = import.meta.env.VITE_SUPABASE_URL
const supabaseKey = import.meta.env.VITE_SUPABASE_ANON_KEY

export const supabase = createClient(supabaseUrl, supabaseKey)
</script>

<template>
  <main>
    <TheWelcome />
  </main>
</template>
