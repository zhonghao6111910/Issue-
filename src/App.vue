<template>
  <div id="app">
    <!-- <Header /> -->
    <!-- <IssueQuery /> -->
    <!-- <CreateNewIssue /> -->
    <!-- <Solution /> -->
    <IssueReport />
  </div>
</template>

<script>
import Login from "./components/Login";
import Header from "./components/Header";
import IssueQuery from "./components/IssueQuery";
import CreateNewIssue from "./components/CreateNewIssue";
import Solution from "./components/Solution";
import IssueReport from "./components/IssueReport";

export default {
  name: "App",
  components: {
    Login,
    Header,
    IssueQuery,
    CreateNewIssue,
    Solution,
    IssueReport
  }
};
</script>
<style>
html {
  padding: 0;
  margin: 0;
}
body {
  padding: 0;
  margin: 0;
}
</style>
