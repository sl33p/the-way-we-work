# General deployment guide

Our main applications are all deployed in slightly different ways, but when deploying anything there are some general rules we should all follow.

## When should I deploy?

Before doing any deployment, think about timing.

_Is there a customer demo happening, now or in the near future?_ It's best not to deploy near a customer demo, just in case any downtime occurs, or if a sudden change in functionality happens mid-demo.

_What time is it?_ If it's near the end of the day, consider putting the deployment off until tomorrow morning (unless you're prepared to stay late and fix up if things go wrong!)

_What day is it?_ It's best to do deployments Monday-Thursday, or Friday morning at a push. Friday afternoon is risky, again due to the possibility of things going wrong and needing to be fixed. No-one wants to be staying late on a Friday!

## How to deploy

Each application has its own deployment guide.

* [Livestax](https://github.com/livestax/livestax#deployment)
* [Javascript API](https://github.com/livestax/livestax-js-api#releasing-a-new-version)
* [Livestax Theme](https://github.com/livestax/theme#deploy)
* [Demo apps for Livestax](https://github.com/livestax/livestax-development-apps#deploying)

You may not have deployment rights to all applications - check with Jamie/Laura if you're not sure.

### Notifications

Before deploying, check with the team that they're happy with a deployment going ahead. Use the #ops channel in Slack to notify the team.

While deploying, keep the team informed during the whole process. Post a message in #ops along the lines of `Starting deployment!` before you begin.

The below are a guide, you can of course use your own words!

### Deploying Livestax (the main Rails app)

Always deploy to staging first:

:performing_arts: `Deploying to staging...`

Once the deployment has completed:

`Deployed to staging... checking`

Then once you've checked staging and are happy with everything:

`Deployment to staging complete`

The next environment you deploy to will be production (NOT sandbox). Repeat the above, but use the emoji for production:

:moneybag: `Deploying to production...`

We deploy Livestax to production before sandbox because sandbox is not currently Dockerised; see [Livestax deploy to production](https://github.com/livestax/livestax#deploy-to-production)

Once your app is deployed to production successfully, you can deploy to sandbox:

:desert: `Deploying to sandbox...`

When all environments are deployed and checked, let the team know:

:tada: `All deploys done!`

### Deploying everything else

For applications other than Livestax, you will want to deploy to sandbox _before_ production.

:performing_arts: `Deploying to staging...`

Once you've checked staging and are happy with everything, deploy to sandbox:

:desert: `Deploying to sandbox...`

Then when you're happy with sandbox, deploy to production:

:moneybag: `Deploying to production...`

When all environments are deployed and checked, let the team know, and get yourself a :beer:

:tada: `All deploys done!`
