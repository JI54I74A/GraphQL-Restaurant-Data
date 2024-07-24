# GraphQL-Restaurant-Data
This is a GraphQL Restaurant Data excersise
# How to Run
In this excersise using GraphQL query and mutation to doing CRUD operations.
For running need to initiate npm, by running this command </br>
`npm init`
 To run the code
 `node index.js`
# Roadmap
Five operations can do using this code in Qraphql Playground</br>
**READ - single**</br>
restaurant: This gets a single restaurant based on a provided ID.</br>
Qraphql Playground Query</br>
```
query findrestaurants($iid:Int=1){</br>
  restaurant(id: $iid) {</br>
    name
    description
    dishes{
      name
      price
    }
  }
}
```
**READ - all**</br>
restaurants: This gets a list of all restaurants. </br>
Qraphql Playground Query</br>
```{
  restaurants {
    name
    description
    dishes{
      name
      price
    }
  }
}```</br>
**CREATE**</br>
setrestaurant: This creates a new restaurant. </br>
Qraphql Playground Mutation</br>
```mutation setrestaurants {
  setrestaurant(input: {
    name: "Granite",
    description: "American",
  }) {
    name
    description
  }
}```</br>
**DELETE**</br>
Deleterestaurant: This deletes a restaurant based on the provided id.</br>
Qraphql Playground Mutation</br>
```mutation deleterestaurants($iid: Int = 1) {
  deleterestaurant(id: $iid) {
    ok
  }
}```
**UPDATE/EDIT**</br>
editrestaurant: This updates a restaurant based on the provided id.</br>
Qraphql Playground Mutation</br>
```mutation editrestaurants($idd: Int = 1, $name: String = "OLDO") {
  editrestaurant(id: $idd, name: $name) {
    name
    description
  }
}```
# License
MIT License

Copyright (c) 2020 John Williams

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

