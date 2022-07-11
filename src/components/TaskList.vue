<template>
    <div>
       <span>{{ name }}</span>
       <button @click="updateProfile">Thay doi ten</button>
    </div>
</template>

<script>
import { mapActions, mapGetters, mapMutations } from 'vuex'

export default {
    props: ['tasks'],
    computed: {
        ...mapGetters(['name'])
        // chuyen store.state.name thanh this.name
    },
    methods: {
        ...mapMutations(['setName']),
        // lay ham setname tu mutations cua store ve this(component hiện tại)
        ...mapActions(['updateProfile']),
    }        
}
</script>
