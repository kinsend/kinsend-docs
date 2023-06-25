# Gathering Requirements

Gathering requirements is of key importance when you need to plan, organize and distribute work.
When raising bugs and tasks in the issue tracker, it's important to be able to describe in a clear and concise way
what the problem is and what exactly needs to be done, so that anyone in the team could pick up the work and have
as much information and resources, as necessary in order to be able to work out the finer details independently.

When the overall duration of the task is estimated to be longer than just a few days, it's important to have clarity
on what the list of sub-tasks is and to keep the progress visible, so that others could join in and easily help push
things forward without overlapping efforts, or the need for lengthy explanations on how they can help. This could be
crucial, if the completion of the task is required in a significantly shortened time-frame. Also, as we all know,
everything happens in life (people get, go on vacation, or quit) and without such clarity, it would take an additional
effort to evaluate the progress of the task, should the original assignee be re-assigned, or not be able to complete
the work.

## How to gather requirements

This is a short list of things to keep in mind when gathering requirements, so that they could be well-defined
and easy to handover:

* __Task Description (Mandatory)__

    Make a rough outline of the problem (use bullet points to force yourself to be brief, but at the same time try 
    to provide a sufficiently clear explanation).

    As soon as you have gained an initial understanding of the overall task, try to outline the main parts of the work
    that needs to be done, so that you could later dive into the finer details.

    Define what the "definition of done" is, so that you could later evaluate the progress of the work and draw a line,
    when the work is completed.

* __Task List (Mandatory)__

    Expand on each bullet point with sub-points, until the amount of detail is sufficient, but stick
    to the point and don't add excessive details

    This will help improve the understanding of what needs to be done and provide more granularity.

    Gather a list of documentation resources that will need to be updated, (if any), as our documentation needs to be
    continuously improved.

* __Open Questions (Optional)__

    If there are any open questions, or things that you are not sure about, make sure to list them, so that you could
    later discuss them with the team and get the answers you need.

* __Notes (If Applicable)__

    As you progress with the work, make sure to keep notes of the things you have learned, so that you could later
    share them with the team and help them get up to speed with the work. This often helps when follow-up tasks
    are required, because they might be done by someone else, who might not have the same level of understanding and
    it would be easier for them to get up to speed with the work, if they have access to the notes.

* __Useful Commands (If Applicable)__

    Continuously add useful commands and output (when working on the task). This will help:

    * Other people join in and help you, or continue your work, if necessary, as it will reduce the
      amount of time they need to spend on figuring out how to do things you've already figured out.

    * You not waste time to figure out that three line script you knocked up yesterday that you used to check some data.

* __Incurred Costs (If Applicable)__

    If you are working on a task that will incur costs, try to understand them and provide a rough estimate, so that
    it could be taken into account when planning the budget.

* __Task Relationships__

    If the task is related to other tasks, make sure to list them, so that it's clear what the relationships are.

* __Resources (If Applicable)__

    List resources that are related to this task. This will help you and others to quickly find the resources that are 
    related to the task, without having to search for them.

    For example, list things like:
    
    * IP-s
    * Subnets
    * DNS records
    * ARN-s
    * S3 buckets
    * Names of secrets in the AWS Secret Manager or `.env` files (not their actual values, of course)

* __Useful Links (If Applicable)__

    This is extremely important for continuity and handovers, as it will help others get up to speed with what you
    have already researched. Gather links to:

    * Articles
    * Documentation
    * Discussions on forums and mailing lists
    * StackOverflow questions
    * GitHub issues
    * GitHub pull requests

* __Points of Contact (Mandatory)__

    Outline the points of contact (requested by, SME[^1]-(s) on this topic, mailing lists, forums, chat channels)

    * This will help you find more information, or get hints, if you get stuck.

    * Feel free to ask questions on Stackoverflow, there are many people out there who could help, or provide
     a different angle to view things from.

## Additional Recommendations

When the requirements are gathered, identify the larger pieces of work and split them into new tasks, if necessary
(repeat the requirements gathering process and apply it to them as necessary).

As work progresses on a given task, sometimes new requirements pop up that will increase the time required to
complete it. So, when it makes sense, extract the work into separate new tasks.

   * Keeping the overall task as something easy to achieve, improves the morale, as it increases the sense
      of achievement.

   * Lengthy tasks have the following undesired side-effects:
      
       * Reviewing the code will take a while
       * You might have to rebase several times and waste time resolving conflicts

Here are some example tasks that follow these principles:

* [kinsend/tf-kinsend#6](https://github.com/kinsend/tf-kinsend/issues/6)
* [kinsend/tf-kinsend#21](https://github.com/kinsend/tf-kinsend/issues/21)
* [kinsend/tf-kinsend#8](https://github.com/kinsend/tf-kinsend/issues/8)
* [kinsend/tf-kinsend#11](https://github.com/kinsend/tf-kinsend/issues/11)
* [kinsend/tf-infrashared#11](https://github.com/kinsend/tf-infrashared/issues/11)

[^1]: SME: Subject Matter Expert
