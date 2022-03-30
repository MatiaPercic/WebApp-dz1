<template>
  <div id="app">
    <ul id="example-1">
        <li v-for="commit in this.commits" :key="commit">
            Commit: <router-link to="/details/sha" @click="setCommit(commit.sha)">{{ commit.sha }}</router-link>
        </li>
    </ul>
  </div>
</template>

<script>

import axios from 'axios';

export default {
  name: 'GetCommit',
  props: {
    url: URL
  },
  data() {
        return { commits: [] }
    },
        methods: {
            async getData() {
            try {
                const response = await axios.get(
                "https://api.github.com/repos/vuejs/vue/commits"
                );
                this.commits = response.data;
                } catch (error) {
                    console.log(error);
                }
            },
            parse() {
                console.log(commits);
            },
            setCommit(sha) {
                localStorage.setItem("requestedCommit", sha)
            }
        },
        created() {
            this.getData();
        }
}
</script>