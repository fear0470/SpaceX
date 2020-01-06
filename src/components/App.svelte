<script>
  	import ApolloClient from "apollo-boost";
	import { setClient } from "svelte-apollo";


    const client = new ApolloClient({
    uri: "http://api.spacex/graphql",

    onError: ({ networkError, graphQLErrors }) => {
      console.log("graphQLErrors", graphQLErrors);
      console.log("networkError", networkError);
    }
  });
  setClient(client);
</script>


<style>

</style>

<h1>hello</h1>