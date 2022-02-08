<script>
export default {
    props: ['todo'],
    data() {
        return {
            title: this.todo.title,
            edit: false,
        }
    },
    methods: {
        Edit() {
            this.edit = true
        },
        Save() {
            this.edit = false
            this.$emit('todo-item-changed', {
                original: this.todo,
                new: {
                    title: this.title
                    },
            })
        }
    }
}
</script>

<style>

</style>