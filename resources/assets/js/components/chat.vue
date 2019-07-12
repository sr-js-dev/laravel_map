<script>
export default {

        mounted() {

            this.listen()

        },

        props: ['userId'],

        methods: {

            listen() {

                Echo.private('App.User.' + this.userId)

                    .chat((chat) => {

                        console.log(chat)

                    })

            }

        }

    }
</script>
