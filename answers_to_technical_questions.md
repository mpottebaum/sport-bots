# Answers To Technical Questions

1. I spent a lot of time on the challenge, somewhere around 20 hours on it. I would first add improvements to the user interface. I focused mostly on user experience, making sure the app was intuitive to use. I would start with a better way to display the rosters. I just used Bootstrap's table, but I would like it a lot better if the table headings were fixed. As it is, it's hard to keep track of which columns correspond to which attribute items as you scroll the roster or list of bots.

2. I love destructuring assignment in ES6. I use it often to declutter components and make the code easier to read. Here, I used it in the Player component (used on the Roster page) to declutter the returned JSX:

```
const { name, speed, strength, agility } = player

return (
    <tr>
        <td>{name}</td>
        <td>{speed}</td>
        <td>{strength}</td>
        <td>{agility}</td>
    </tr>
)
```

3. I have not had to do this before. But, to track down issues on the front end, I would start by using Chrome's Performance tool to record processes and pinpoint the source of the issue. On the back end, I would start with the logs and try to identify unnecessary or duplicated database queries, errors, etc.

4. mike.json:
```
    {
        "name": "Mike",
        "favorite_things_this_year": {
            "book": "The Three Body Problem by Cixin Liu",
            "movie": "Palm Springs",
            "podcast": "Two Bears, One Cave",
            "tv_show": "Never Have I Ever",
            "album": "Igor by Tyler, The Creator"
        },
        "musical_instruments": [
            "piano",
            "guitar",
            "bass",
            "drums"
        ],
        "favorite_sport": "basketball"
    }
```