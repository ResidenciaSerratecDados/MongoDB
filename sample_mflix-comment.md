```js

// Primeiro, obter o _id do filme
var movie = db.movies.findOne({ title: "The Dark Knight" });

// Agora buscar todos os comentários desse filme
db.comments.find({ movie_id: movie._id }, {name: 1, text: 1, _id: 0 });

db.comments.find({ movie_id: movie._id }, { year: 1, name: 1, text: 1, _id: 0 }).limit(5);

```