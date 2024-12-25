<!-- App.vue -->
 <template>
    <div id="app">
        <ActiveUser :username="user.name" :age="user.age" />
        <UserData @update-user="handleUpdateUser" />
    </div>
 </template>

<script setup>
console.log('hello from app');
    import { ref } from 'vue';
    import ActiveUser from './components/ActiveUser.vue';
    import UserData from './components/UserData.vue';

    const user = ref({

        name: 'John Doe',
        age: 30
    })

    const handleUpdateUser = (updateUser) => {
        user.value = updateUser;
    };
</script>

<style>
#app {
    display: flex;
    justify-content: space-evenly;
    width: 100%;

    font-family: Avenir, Helvetica, Arial, sans-serif;
    text-align: center;
    margin-top: 60px;
}
</style>