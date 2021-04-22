<template>
    <form class="add-form">
        <div class="form-control">
            <label>Task</label>
            <input type="text" v-model="text" name="text" placeholder="Add Task" />
        </div>
        <div class="form-control">
            <label>Day and Time</label>
            <input type="text" v-model="day" name="day" placeholder="Add Day and Time">
        </div>
        <div class="form-control form-control-check">
            <label>Set Reminder</label>
            <input v-model="reminder" type="checkbox" name="reminder" />
        </div>
        <input type="submit" value="Save Task" class="btn btn-block" />
    </form>
</template>

<script>
export default {
    name: 'AddTask',
    data() {
        return {
            text: '',
            day: '',
            reminder: false
        }
    }
}
</script>

<style scoped>
.add-form {
    margin-bottom: 2.5rem;
}
.form-control label {
    display: block;
}
.form-control input {
    width: 100%;
    height: 40px;
    margin: .5rem;
    padding: 3px 7px;
    font-size: 1.1rem;
}
.form-control-check {
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.form-control-check label {
    flex: 1;
}
.form-control-check input {
    flex: 2;
    height: 1.5rem;
}
</style>
