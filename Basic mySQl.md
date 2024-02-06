First is create the basic `index.html`.
```html
<!doctype html>

<html lang="en">

  <head>

    <meta charset="UTF-8" />

    <link rel="icon" type="image/svg+xml" href="/vite.svg" />

    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <title></title>

    <link rel="stylesheet" href="style.css">

  </head>

  <body>

    <main>

      <label for="name">Name:</label>

      <input type="text" name="Name" id="name-input">

      <button id="add-name-btn">Add name</button>

  

      <div>

        <input type="text" name="name-search" id="search-input" placeholder="Search by name">

        <button id="search-btn">Search</button>

      </div>

  

      <table id="table">

        <thead>

          <th>id</th>

          <th>Name</th>

          <th>Date added</th>

          <th>Delete</th>

          <th>Edit</th>

        </thead>

        <tbody id="tbody">

  

        </tbody>

      </table>

    </main>

    <script type="module" src="/main.js"></script>

  </body>

</html>
```

Next is the `style.css`:
```css
*,

*::after,

*::before{

  all:unset;

}

  

h1{

  color: black;

  font-family: 'Poppins', sans-serif;

}

input{

  border: 1px solid black;

}

  

main{

  display: grid;

  place-content: center;

  height: 100vh;

  gap: 2rem;

}

button{

  border: 1px solid black;

  background-color: azure;

  cursor: pointer;

}

table{

  display: flex;

  flex-direction: column;

}

th{

  border: 1px solid black;

}
```

Next is install all the libraries:
```bash
npm init -y
npm i express
npm i mysql
```

