# Workflows

- workflows
- notifications
- data flows + github/netlify?

Workflows are a way to add structured stages to the flow of content authoring. They are primarily defined through the
permissions for a Collection, but can be further enhanced via email notifications, custom interfaces, and
[flows](/configuration/flows.md).

<video title="Configure Workflows" autoplay playsinline muted loop controls>
	<source src="https://cdn.directus.io/" type="video/mp4" />
</video>

1. To create a structured workflow for **Articles**, the first step is
   [Creating a Field](/configuration/data-model#creating-a-field) to track the article status — we'll call it `status`,
   but it can be named anything.
2. Next, create different roles for each stage of the workflow, such as `author` and `manager`.
3. Finally, configure the role permissions based on the possible values of that `status` field, such as `draft`,
   `review`, `approved`, and `published`, so that they are properly restricted to create content and update the status.
   - The Author can create content, but only save a status of `draft` or `review`.
   - The Manager has additional permissions that allow them to save statuses of `approved` or `published`.