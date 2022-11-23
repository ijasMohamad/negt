# negt

<br>
CLI-App can auto generate graphql models and resolvers by your requirements.. <br>
For example :- If you want to make graphql models and it's resolvers please provide the details for the questions.<br>
It will auto generate graphql schema and resolvers by itself.

<h2><b>Quick Start</b></h2>

1. <a href="https://golang.org/doc/tutorial/create-module">Initailise a new go module</a>

    mkdir example
    cd example
    go mod init example

2. Add negt package to your module.
    
    go get github.com/ijasMohamad/negt@latest
     
3. For installing negt,
 
    go install github.com/ijasMohamad/negt@latest

This will install the `negt` command to your `$GOPATH/bin` directory.

<h2><b>Usage</b></h2>
    
1. For seeing the command options in the terminal,
  
    negt

    negt help
  
    negt gqlgen
    
2. Then for initializing GraphQL models
 
    negt gqlgen init
    
It will create directories 'gql/models'.
  
3. Then for creating new GraphQL model 
  
    negt gqlgen model
    
You will get some questions, please provide the details for the questions.<br>
It will create GraphQL Model files in "gql/models/<modelName>".

    Files :-
        1. index.js :- It contains all relations of the gql model.
        2. models.js :- It contains fields and GraphQLObjectType of the model.
        3. query.js :- It contains query of the model.
        4. list.js :- It contains connection and query list of the model.
        5. mutation.js :- It contains the mutation fields and mutation object.
        6. customCreateMutation.js :- If you need custom resolvers for the GraphQL model, you can say yes for the question in the CLI.
           If you said yes, then it will create 3 custom resolver files. This file contains the custom create mutation object.
        7. customUpdateMutation.js :- It contains the custom update mutation object.
        8. customDeleteMutation.js :- It contains the custom delete mutation object.
    
It will create its test files also in "gql/models/<modelName>/tests",
    
    Test files :-
        1. index.test.js :- It contains the test cases of index.js file. It checks the importing is working properly.
        2. models.test.js :- It contains the test case for type of the GraphQL model.
        3. query.test.js :- It contains the test case of GraphQL query.
        4. list.test.js :- It contains the test case of GraphQL query list.
        5. mutation.test.js :- It contains the test cases of GraphQL mutations like creating, updating and deleting.
        6. pagination.test.js :- It contains the test case for checking the pagination of GraphQL queries is working properly.
           Most of the case, we don't need to change this file anymore. So it will create this test case in a different file.
        7. customCreateMutation.test.js :- It contains the test case of custom create mutation resolver.
        8. customUpdateMutation.test.js :- It contains the test case of custom update mutation resolver.
        9. customDeleteMutation.test.js :- It contains the test case of custom delete mutation resolver.

Also, it will create mockData file for the model in utils/testUtils directory.


<h3>Wednesday Solutions &copy;</h3>
