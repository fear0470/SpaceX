<script>
  	import ApolloClient from "apollo-boost";
	import { setClient } from "svelte-apollo";
	import Header from "./ui/Header.svelte";
	import Footer from "./ui/Footer.svelte";


    const client = new ApolloClient({
    uri: "http://api.spacex.land/graphql",

    onError: ({ networkError, graphQLErrors }) => {
      console.log("graphQLErrors", graphQLErrors);
      console.log("networkError", networkError);
    }
  });
  setClient(client);
</script>


<style>

</style>
<Header />
<h1>hello</h1>
<Footer />