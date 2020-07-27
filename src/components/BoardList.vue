<template>
    <table class="table">
        <thead>
            <tr>
                <th>번호</th>
                <th>제목</th>
                <th>작성자</th>
                <th>작성일</th>
                <th>조회수</th>
                <th>추천수</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="item in list">
                <td>{{item.index_no}}</td>
                <td>{{item.title}}</td>
                <td>{{item.writer}}</td>
                <td>{{item.reg_dttm}}</td>
                <td>{{item.read_count}}</td>
                <td>{{item.recommend_count}}</td>
            </tr>
        </tbody>
    </table>
</template>

<script lang="ts">
    import {Component, Vue} from 'vue-property-decorator';

    @Component
    export default class Board extends Vue
    {
        list: Array<Object> = [];
    }
</script>