<!-- @format -->

<template>
    <div class="todos">
        <div class="select" v-for="value in posts">
            <div>{{ value.title }}</div>
            <button @click="deleteFunc(value.id)">Delete</button>
        </div>
    </div>
</template>
<script>
export default {
    props: {
        posts: {
            type: Array,
            required: true,
        }
    },
    methods: {
 
    },
};
</script>
<style scoped>
.todos {
    min-height: 300px;
}

.select {
    border: 3px solid darkseagreen;
    padding: 5px 10px;
    width: 90%;
    margin: 10px auto;
    font-size: 22px;
    display: flex;
    justify-content: space-between;
    border-radius: 5px;
}

.select>button {
    background-color: none;
    border: 2px solid darkseagreen;
    max-width: 200px;
    font-size: 17px;
    padding: 4px 10px;
    cursor: pointer;
    font-weight: 600;
    justify-self: end;
    transition: 0.1s;
    border-radius: 5px;
}

.select>button:active {
    transform: scale(1.1);
}
</style>
