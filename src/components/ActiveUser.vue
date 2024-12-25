<!-- ActiveUser.vue -->
 <template>
    <div>
        <h2> {{ username }} </h2>
        <h3> {{ age }} </h3>
    </div>
 </template>

 <script setup>
    console.log('hello from active user');
    import { defineProps } from 'vue';


    const props = defineProps({
        username: {
            type: String,
            required: true
        },
        age: {
            type: Number,
            required: true
        }
    });
    console.log(props);
</script>

<style scoped>
    h2 {
        color:blue;
    }
    h3 {
        color: green;
    }
</style>