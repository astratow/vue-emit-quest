<!-- UserData.vue -->
 <template>
    <div>
        <input v-model="name" placeholder="Enter Name" />
        <input v-model="age" type="number" placeholder="Enter Age" />
        <button @click="updateUser">Update User</button>
    </div>
 </template>

 <script setup>
    import { ref, defineEmits } from 'vue';

    const name = ref('');
    const age = ref(null);

    const emit = defineEmits(['update-user'])
    const updateUser = () => {
        if (name.value && age.value) {
    emit('update-user', { name: name.value, age: age.value });
  } else {
    alert('Please enter both name and age.');
  }
    };
</script>

<style scoped>
input {
  display: block;
  margin-bottom: 10px;
}
button {
  background-color: #4CAF50;
  color: white;
  border: none;
  padding: 10px;
  cursor: pointer;
}
button:hover {
  background-color: #45a049;
}
</style>