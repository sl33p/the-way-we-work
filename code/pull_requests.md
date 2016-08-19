# Pull requests

## Why we do pull requests

It would be quickly catastrophic if we committed straight to master all the time. Why?

- It'd make it harder to see nice atomic chunks of work
- You would tread on other peoples code toes
- It would be more work and harder to roll back/revert a feature or change.
- There'd be no opportunity to benefit from the collective knowledge and experience of the team

The benefits to doing pull requests are:

- allow others to explore the consequences of a change
- share information about what is changing
- provide an opportunity for the team to help spot any potential oversights/shortcomings
- provide an insight into how others have solved a problem/implemented a feature enabling you to learn from their experience
- provide an opportunity to collaborate on improvements

## General guidance

- Don't rely on someone else to spot and merge your pull requests - it's your job to find a reviewer and get the code merged
- A piece of work can be split into multiple pull requests

## Opening a request

- Before opening the PR, make sure you're up to date with `master` so that your changes are easier to merge.
- The title and description should help the reviewer. Make the title succinct and descriptive, and then add detail in the description
- The description should summarise your changes and include useful links, eg to related pull requests. If the changes result in visual changes, screenshots are really useful
- When raising a PR, the title and description are emailed to those following the repo. Any subsequent changes are not emailed, so it's worth spending a bit of time getting it right at the point of raising the PR.
- It is worth explaining/highlighting any potentially contentious changes, and any testing that you have already done.

Note: The canonical description of changes should always be in the individual
commits - Pull Requests are an artefact of GitHub, and we would lose that data
if we switched away. Please refer to the [commit message
styleguide](/git.md#commit-messages).

## Reviewing a request

### Guidelines for review

- It is important to take time to review a pull request properly; the review stage is as important as writing the code in the first place
- If you're not sure how the individual wants their request reviewed, ask them before starting - they may prefer some of the feedback to be done in person or while pairing (especially if they're less experienced)
- If the code is good, or solves something in a clever way, *say so*. Call out individual bits of quality - it signposts good practice for others, and rewards the person submitting the request.
- State what, if anything, is a blocker explicitly


### Helpful things to consider while reviewing

- Try running the code - even if the tests pass it might have bugs
- Remember that a PR does not have to entirely solve the problem. If it adds value on its own it might be better to merge now rather than wait for the rest
  of the changes required.
- Always comment on individual lines in the full-file diff view, not on a commit page because they will be lost if a rebase happens
- Check that any relevant documentation (`README` files, things in the `doc` folder) is up to date with the changes


### Addressing comments

- If you're changing something minor in an existing commit (eg renaming a variable for clarity, adding a missing test), amend the existing commit (please ask for help if you don't know how to do this)
- If the best way of making a change in response to feedback is a separate commit, "Addressed feedback" isn't an acceptable commit message
- Explicitly comment that all relevant comments have been addressed to notify any watchers - you don't need to do this on a per-comment basis


## Further reading

- [Anna Shipman](https://github.com/annashipman) has written a useful blog post about [how to raise a good pull request](http://www.annashipman.co.uk/jfdi/good-pull-requests.html)
- A great example of [a good pull request](https://github.com/alphagov/frontend/pull/784) raised by [Alice Bartlett](https://github.com/alicebartlett)
