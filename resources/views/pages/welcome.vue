<script setup lang="ts">
const form1 = useForm({
    url: '/form1',
    method: 'POST',
    fields: {
        field1: ''
    }
})

const form2 = useForm({
    url: '/form2',
    method: 'POST',
    fields: {
        field2: ''
    }
})
</script>

<template>
    <div>
        <form @submit.prevent="form1.submit()">
            <input type="text" name="name" v-model="form1.fields.field1">
            <button>Submit Form 1</button>
        </form>

        <form @submit.prevent="form2.submit()">
            <input type="text" name="name" v-model="form2.fields.field2">
            <button>Submit Form 2</button>
        </form>
    </div>
</template>
