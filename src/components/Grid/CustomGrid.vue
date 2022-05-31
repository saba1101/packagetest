<template>
    <div class="grid-wrapper">
        <div class="grid">
            <div class="grid-header">
                <div class="col" v-for="(col,ind) in props.columns" :key="ind">
                    <span class="col_value">
                        {{col.title}}
                    </span>
                </div>
            </div>
            <div class="grid-body">
                <div class="col" v-for="(obj,ind) in data" :key="ind" @click="clickedRow(obj)">
                    <div class="row" v-for="(col,index) in props.columns" :key="index">
                        <span class="col_value">
                            {{filterDataByColumn(obj,col)}}
                        </span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import {defineProps,defineEmits,} from 'vue'
    const props = defineProps({
        data: Array,
        columns: Array,
    })
    const emit = defineEmits(
        [
            'clickedRow'
        ]
    )
    const filterDataByColumn = (obj,col) => {
        return obj[col.identifier]
    }
    const clickedRow = (row) =>{
        emit('clickedRow',row)
    }
</script>

<style lang="scss" scoped>
    .grid-wrapper{
        width: calc(100% - 12rem);

        .grid{
            width: 100%;
            display: flex;
            justify-content: flex-start;
            align-items: left;
            flex-direction: column;

            .grid-header,.grid-body{
                width: 100%;
                display: flex;
                flex-direction: row;
                justify-content: left;
                align-items: center;

                .row{
                    width: 100%;
                    overflow: hidden;
                    color: #fff;
                    text-overflow: ellipsis;
                    white-space: nowrap;
                    margin-left: 1.5625rem;
                    &:first-child{
                        margin-left: 0;
                    }
                }
                .col{
                    width: 100%;
                    text-align: left;
                }
            }

            .grid-header{
                padding: 0.9375rem 1.5625rem;
                position: sticky;
                top: 0;
                background: lighten(#3d3d3d,25%);
                border-radius: 0.3125rem;
                border-bottom-left-radius: 0;
                border-bottom-right-radius: 0;


                span{
                    color: #fff;
                    font-weight: 700;
                    font-size: 0.875rem !important;
                }

                .col{
                    margin-left: 1.5625rem;
                    &:first-child{
                        margin-left: 0;
                    }
                }
            }
            .grid-body{
                flex-direction: column !important;
                align-items: flex-start;
                padding-top: 0;
                border-bottom-left-radius: 0.3125rem;
                border-bottom-right-radius: 0.3125rem;
                user-select: none;
                span{
                    color: rgba(#fff,.7);
                    font-weight: 500;
                }
                .col{
                    display: flex;
                    justify-content: flex-start;
                    align-items: ceter;
                    flex-direction: row;
                    padding: 1.25rem 1.5625rem !important;
                    transition: all .2s;
                    background: #3d3d3d;
                    border-bottom: 1px solid rgba(#fff,.1);
                    &:hover{
                        background: lighten(#3d3d3d,35%);
                    }
                }
            }
        }
    }
</style>



