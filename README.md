# Website Planning

A lot of this will be Stream of Consciousness (SOC). I will distill these into system specs later.

Frontend. One frontend? A main frontend plus others?

Main one will be Nuxt. SSG is mature now, so there's no reason not to. Astro's great, but I'm using Vue exclusively at the moment; my metaframework should reflect that.

Sections
- Header
- Portfolio (coming soon)
- Blog (coming soon)
- Contact Form (coming soon)
- Feedback (coming soon)

Components
- Coming Soon placeholder widget

Cypress for integration testing. Vitest for unit testing.

## Infrastructure

This will be IaC. Learn Terraform. Kubernetes? Likely not; overkill. Terraform yes.

AWS. Put that certification to work. Secrets Manager, SDK, EC2, SQS, the works. Maybe SES too; run a Budget once the sys spec is crystallized.

Multiple repos, one orchestrator. Repos:
- Website_Frontend
- Website_Deployment
- Website_ContactFormWidget
- Website_FeedbackWidget

Updates to main branch of a child repo should trigger a build action in its Parent. Let's say, for example, that Frontend depends on ContactFormWidget. Changing ContactFormWidget's main branch should trigger Frontend to be rebuilt and redeployed.

Transfer domains from GoDaddy to Route 53.