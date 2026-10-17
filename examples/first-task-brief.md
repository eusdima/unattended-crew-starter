# Example first-task brief

You do not need a formal brief. You type a request in plain English and the first mate turns it into the worker's instructions. A good request still has the same four parts, so give them up front and the worker needs fewer questions.

## The request

```text
In your-site, the "Contact" link in the footer goes to /contct and returns a 404.
Fix it so it goes to /contact. Change only that link. Open a pull request
and tell me what you changed.
```

## What each part does

- **Where**: the project and, if you know it, the file or page. Here, the footer of `your-site`.
- **What is wrong, or what you want**: observable, so the worker can check it. A 404 on a link is checkable. "Make the footer better" is not.
- **Limits**: what to leave alone. "Change only that link" keeps the pull request small enough to read in a minute.
- **What done looks like**: a pull request you can review, with a plain summary.

## Good first tasks

- Fix a broken link
- Fix a typo on one page
- Add missing alt text to one image
- Update a copyright year in a footer

## Poor first tasks

- Anything that touches payments, accounts or customer data
- Anything you could not review in a few minutes
- Anything that spends money or publishes something public

## Try it on the example project

[`minimal-project/`](minimal-project/) contains a tiny site with exactly this bug. Push it to a new GitHub repository of your own, add that repository to your first mate, and use the request above with your own repository name.
