# Dynamyk site project [TEAM BDIM]

## Authors

* Dan [@plasticneuron](https://github.com/plasticneuron)
* Reda [@redahaq](https://github.com/redahaq)
* Pat [@pat-cki](https://github.com/pat-cki)
* Beth [@bethanyios](https://github.com/bethanyios)

## Motivations

Our purpose was simple: to learn as much as we could, to build a pretty website, and not to kill each other in the process... Peace and love y'all.

![godzilla loves you](http://giphygifs.s3.amazonaws.com/media/DrQsEteT3ngBO/giphy.gif)

## Process

### First steps

We began by closing our laptops, looking through the [design brief](https://github.com/foundersandcoders/master-reference/blob/master/coursebook/week-1/project.md), talking through our ideas for the site and looking for consensus on key design questions.

![no I in team](https://media.giphy.com/media/3rgXBrLlRs4ZlpnVDO/giphy.gif)

One of these decisions was to design **mobile-first** and then design for other devices (principally desktop) via _progressive enhancement_. For us, this looked like responsive elements and a media query with a min-width of 600px.

We also decided together to use **Beautify** to render all our code in the same manner.

To make sure we had a good shared understanding of the overall structure of the wesbite, and to avoid having to deal with too mnay conflicts, we produced sketches of the wireframe and content:

![wire frame of site](https://i.imgur.com/xmGfL9p.jpg) ![content sketching](https://i.imgur.com/spP57x2.jpg)


We then mob-built the HTML structure, trying to make it as semantic as possible. This resulted in our [first commit](https://github.com/fac18/dynamyk-site/commit/c0761cecbdcbc8130a51e0656e847fde903e5cf4) beyond initialisation. Only after that did we begin to work on different features in pairs, with branches.

### Tracking our progress

We used this list to keep track of whether we were meeting the design brief specified by the user stories. On visiting the site, a client/site user should be able to:

- [x] immediately see a headline about our team
- [x] immediately get a concise description of the services we offer
- [x] see for a nav including About, Team and Contact sections
- [x] be able to navigate to these locations by clicking these
- [x] be able to contact us by filling out a form, including name, email and a message
- [x] this information should be sufficient for us to contact them
- [x] be able to click on nav links and end up at the appropriate part of the page
- [x] not have to wait for new pages to load
- [ ] easily view site on mobile, desktop and tablet
- [ ] easily understand the site's contents from whichever device they use
- [ ] easily read and understand text if using a screen reader
- [ ] be able to understand what information is available when using a screen reader
- [x] get a similar experience with or without Javascript
- [x] not feel like they're in the stone age due to reduced functionality without JS

However, due to the exigencies of first-project-speed-production, the features we were building in to actually meet this brief weren't recorded in such nice markdown...

![features to branch](https://i.imgur.com/o6r0Akc.jpg)

A better way of handling our branch/feature production line would've been to **open issues** in our GitHub repo. Commits can then be related to issues (e.g. `relate #5`) to lend further clarity to the repo history.

### Stretch goals

We landed on some stretch goals that we wanted to implement beyond the key design requirements given by the user stories. Some of these were:

- [ ] Making our profiles into on-click flip-cards
- [ ] Integrating the contact form to fill a Google Sheet
- [x] Including a portfolio of actual previous work (the pre-requisite projects)
- [ ] Including a section with testimonials from fabricated previous clientele
- [x] Installing a parallax (non-scrolling) background
- [ ] Add jazzy CSS tricks to the page, just for the hell of it

As you can see, we didn't manage all of them, but they represent design ambitions we'd like to fulfil and likely would have with more time. Shoot for the moon!


### Git flow

Mastering git flow was a key problem we had to manage.

So that we never forget, we'll distil it here for all to see!

The quote blocks represent activity outside of the command line (probably on our project on VS Code or Atom, or on the GitHub repo itself).

So, assuming you've already `git clone`'d the repo sometime in the past, and you've already navigated to the appropriate working directory, the full cycle is as follows:

```bash
git checkout master
git pull origin master
git checkout -b new-branch
```

> build the feature or making the edits for the new-branch

```bash
git add .
git commit -m 'description of changes made'
git checkout master
git pull
git checkout new-branch
git merge master
```

> resolve conflicts emerging from the merge, if any

```bash
git commit -m 'resolved conflicts from merge'
git push origin new-branch
```

> make pull request on GitHub comparing master with new-branch
> wait for team to approve (or request amendments to and resolve) the pull request

```bash
git checkout master
git pull origin master
```

Now your new-branch has been folded in to the master branch, and your spangly new feature is available to everyone, without ruining anyone elses day with a 2 hour code merge ;)

![the reality of merging](https://media.giphy.com/media/cFkiFMDg3iFoI/giphy.gif)

NB. Obviously all these commands would in practice be regularly interspersed with the one and only `git status` to really get a handle on the position of the _HEAD_, relationship to most recent origin/master pull, the state of working directory versus the staging area, etc.
