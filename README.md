# Genius

[Production link][production]

[production]: https://so-genius.com 

## Minimum Viable Product

Genius is a web application inspired by Genius that will be built using Ruby on Rails and React.js.  By the end of Week 9, this app will, at a minimum, satisfy the following criteria:

- [ ] Hosting on Heroku
- [ ] New account creation, login, and guest/demo login
- [ ] A production README, replacing this README
- [ ] Songs with Lyrics
  - [ ] Smooth, bug-free navigation
  - [ ] Adequate seed data to demonstrate the site's features
  - [ ] Adequate CSS styling
- [ ] Annotations on Lyrics
  - [ ] Smooth, bug-free navigation
  - [ ] Adequate seed data to demonstrate the site's features
  - [ ] Adequate CSS styling
- [ ] Comments on Annotations and Songs
  - [ ] Smooth, bug-free navigation
  - [ ] Adequate seed data to demonstrate the site's features
  - [ ] Adequate CSS styling
- [ ] Upvotes on Songs, Annotations, Comments
  - [ ] Smooth, bug-free navigation
  - [ ] Adequate seed data to demonstrate the site's features
  - [ ] Adequate CSS styling

## Design Docs
* [View Wireframes][views]
* [React Components][components]
* [Flux Cycles][flux-cycles]
* [API endpoints][api-endpoints]
* [DB schema][schema]

[views]: docs/views.md
[components]: docs/components.md
[flux-cycles]: docs/flux-cycles.md
[api-endpoints]: docs/api-endpoints.md
[schema]: docs/schema.md

## Implementation Timeline
one feature at a time. Refer back to your MVP and group the features into logical phases. You should have a working app at the end of each phase (even if not all of your features are in yet). For each phase, write a brief game plan and list out any third-party APIs, front-end and back-end components you will need to implement.

### Phase 1: Backend setup and Front End User Authentication (.5 day, W1 Tu 2pm)

**Objective:** Functioning rails project with Authentication

- [ ] create new project
- [ ] host on Heroku
- [ ] create `User` model
- [ ] authentication
- [ ] user signup/signin pages
- [ ] blank landing page after signin

### Phase 2: Songs Model, API, and basic APIUtil (.5 day, W1 Tu 6pm)

**Objective:** Songs can be created and read through the API.

- [ ] create `Song` model
- [ ] seed the database with a small amount of test data
- [ ] CR API for songs (`SongsController`)
- [ ] jBuilder views for songs
- [ ] setup Webpack & Flux scaffold
- [ ] setup `APIUtil` to interact with the API
- [ ] test out API interaction in the console.

### Phase 3: Flux Architecture and Router (1.5 day, W1 Th 6pm)

**Objective:** Songs and their lyrics can be browsed with the user interface.

- [ ] setup the flux loop with skeleton files
- [ ] setup React Router
- implement each song component, building out the flux loop as needed.
  - [ ] `SongDisplay`
  - [ ] `SongDisplayItem`
  - [ ] `SongsIndex`
  - [ ] `SongsIndexItem`
  - [ ] `SongForm`
  - [ ] `Song`
  - [ ] `LyricsDisplay`
  - [ ] `Lyrics`
  - [ ] `SongInfo`
  - [ ] `SongInfoStats`
  - [ ] `SongAbout`

### Phase 4: Start Styling (0.5 days, W2 F 12pm)

**Objective:** Existing pages (including signup/signin) will look good.

- [ ] create a basic style guide
- [ ] position elements on the page
- [ ] add basic colors & styles

### Phase 5: Annotations (2 days, W2 Tu 12pm)

**Objective:** Annotations belong to Songs, and can be viewed by portion of site lyrics.

- [ ] create `Annotation` model
- build out API, Flux loop, and components for:
  - [ ] Annotation CRUD
  - [ ] triggering annotation suggestion (upgrade Lyrics component)
  - [ ] associating annotations with positions in lyrics
  - [ ] activating sections of lyrics as links (upgrade Lyrics component)
  - [ ] viewing annotations by section of lyrics

### Phase 6: Comments (1 days, W2 W 12pm)

**Objective:** Songs and Annotations can be commented on. Comments can be added, edited and destroyed.

- [ ] create `Comment` model (polymorphic)
- [ ] create `Commentable` module and integrate with Songs and Annotations
- build out API, Flux loop, and components for:
  - [ ] fetching comments for songs and annotations
  - [ ] adding / deleting comments on Songs and Annotations
  - [ ] editing comments

### Phase 7: Styling II (1 day, W2 Th 6pm)

**objective:** Annotations and Comments appear in correct places, match Genius style;

- Build layout of lyrics, annotations and comments
  - [ ] Apply style guide to new elements
  - [ ] Style new elements

### Phase 8: Upvotes (1 day, W2 F 6pm)

**objective:** Users can up and downvote songs, annotations and comments. Comments appear in order of upvote count.

- [ ] create `Vote` model (polymorphic)
- [ ] create `Votable` module and integrate with Songs, Annotations and Comments
- build out API, Flux loop, and components for:
  - [ ] fetching vote count and voted status for songs, annotations and comments
  - [ ] voting and unvoting on songs, annotations and comments
  - [ ] ordering comments and top songs by votes (using Rails model)
- [ ] Style the new voter elements.

### Phase 9: Styling Cleanup and Seeding (1 day, W2 Sa 6pm)

**objective:** Make the site feel more cohesive and awesome.

- [ ] Get a large volume of song data, clean and import to database
- [ ] Get feedback on my UI from others
- [ ] Refactor HTML classes & CSS rules
- [ ] Add modals, transitions, and other styling flourishes.

### Bonus Features (TBD)
- [ ] Search
- [ ] Pagination / infinite scroll for SongsIndex and CommentsIndex
- [ ] Tagging
- [ ] Music Player

[phase-one]: docs/phases/phase1.md
[phase-two]: docs/phases/phase2.md
[phase-three]: docs/phases/phase3.md
[phase-four]: docs/phases/phase4.md
[phase-five]: docs/phases/phase5.md
