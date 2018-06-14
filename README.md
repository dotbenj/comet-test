Hi !

This is an off-site test for Backend Engineer in the process of joining the comet team.

# Context

At comet, we handle thousands of freelancers, each freelancers has several professional experiences populated in their profile.

We use these professional experiences in our matching algorithm to match the freelancer with the most relevant experience to the mission.

You can find an example of a mission and of a freelancer data model in the `/examples` folder.

# Exercise

In our matching algorithm, we use the total months of experience of each skill for each freelancer.

If you look at the example, you will see that the freelancer has 3 professional experiences, you can see that he has been doing Javascript since his first professional experience, in may 2013 and kept doing Javascript until his last professional experience in may 2018.

We would like to compute the total number of months the freelancer has worked with each skill.

In this case, we would have :

React: 29 months
Node.js: 29 months
Javascript 29 months + 15 months + 14 months = 58 months
MySQL: 15 months
Java: 15 months + 14 months = 29 months

You will have to read a json file `exercise/freelancer.json`, with the same structure as the example `freelancer.json`.

You will have to compute all of his professional experiences, and output a json with this exact structure :

```
"freelance": {
	"id": 42,
	"computedSkills": [
		{
			"id": 241,
			"name": "React",
			"durationInMonths": 29
		},
		{
			"id": 270,
			"name": "Node.js",
			"durationInMonths": 29
		},
		{
			"id": 370,
			"name": "Javascript",
			"durationInMonths": 58
		},
		{
			"id": 470,
			"name": "MySQL",
			"durationInMonths": 15
		},
		{
			"id": 400,
			"name": "Java",
			"durationInMonths": 29
		}
	]
}
```

# Rules

1. Overlapping months of experience with the same skill(s) should not be counted twice, see [months-overlap.png](./assets/months-overlap.png)
2. All professional experiences `startDate` and `endDate` values will be on the first day of the month.