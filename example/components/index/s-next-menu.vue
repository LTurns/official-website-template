<template>
    <div class="solution-menu">
        <div v-for="(row, index) in data" :key="index" class="menu-row">
            <u-link v-for="(cell, cellindex) in row"  :key="cellindex"
                @click="gotoPage" :to="cell.url"
                class="cell">{{cell.name}}
                <p class="description">{{cell.desc}}</p></u-link>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            data: require('./s-second-menu.json')
        }
    },
    methods: {
        gotoPage() {
            this.$emit('changedNav')
        }
    }
}
</script>

<style lang="scss" scoped>
.description {
    padding-top: 3%;
    font-size: 12px;
    color: grey;
}
.solution-menu {
    padding-bottom: 30px;

    .menu-row {
        display: table-row;
        text-align: center;

        .u-link {
            display: table-cell;
            color: #e6e6e6;
            line-height: 21px;
            padding-top: 30px;
            padding-right: 3%;
            padding-left: 3%;

            &:hover {
                color: #4bb2ff;
            }
        }
    }
}
</style>
