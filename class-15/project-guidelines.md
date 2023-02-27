# Ops 201 Final Project Guidelines

## Conflict Plan

Your team should agree on a process for handing disagreements, should they arise. It is better to have a plan in place ahead of time so you can all refer back to it if necessary.

_Why:_
> Project week can be stressful and emotions can run high. Put together a plan ahead of time so you all know how to deal with any potential issues later.

As a team, create a Group Agreement as a markdown file to document the following:

* What will your group do when it encounters conflict?
* How will you raise concerns to members who are not adequately contributing?
* What is your process to resolve conflicts?
* How and when will you escalate the conflict if your attempts are unsuccessful?

## Communication Plan

Before beginning to tackle the project, determine how your group will communicate with each other.

_Why:_
> This is not an individual effort. Make sure everyone knows how the group will communicate with each other and that everyone feels comfortable speaking up.

Add your communication plan to your Group Agreement. Some things to consider:

* How will you communicate after hours and on the weekend?
* What is your strategy for ensuring everyone's voices are heard?
* How will you ensure that you are creating a safe environment where everyone feels comfortable speaking up?

## Project Scope

Determine which features make up your minimum viable product (MVP). This should include any features you absolutely want to have in your application for presentation day.

_Why:_
> Scope creep can be dangerous! Keeping your project within a pre-determined scope will help the group stay on task without going off on tangents and side features.

Beyond MVP, put together a list of stretch goals to tackle if you have time. During your pitch, your instructor will help you scope your project. Some features may become MVP and some may become stretch goals.

Once you are ready, find your instructor and pitch your idea.

## Daily Team Workflow

As a team, decide how you will work on your project throughout each day.

_Why:_
> Ensure that everyone is on the same page about the current status of the project and the plan for the day.

At the beginning of your day, it is helpful to have a meeting between the team members to make sure that everyone knows what is going on with the project and to discuss the plan for the day. It is wise to have additional check-ins partway through the day and at the end of the day. With every check-in, assess the current percentage of MVP and make a prediction for when your team will reach full MVP.

During your team check-ins, discuss the features each member plans to work on. Determine if the team member will work individually, as a pair, or if the entire team will work on a single feature together, referred to as "mob programming".

Also, use this time to discuss any interpersonal issues that may arise. It is better to address them head-on and resolve any tension rather than allowing it to fester.

## Standup

Every day, the instructional team with circulate to your group for a formal "Standup Meeting". Standup should take approximately 10 minutes per team. Some instructors will opt for a second "Retro meeting" later in the day.

_Why:_
> Standups give the instructional team insight into the current status of your project and the progress the team hopes to make each day.

During standup, each team member will stand up and take turns discussing three points:
>
> 1. What you individually accomplished yesterday
> 1. What you plan to individually accomplish today
> 1. Anything that is blocking you from making progress

## Presentation Prep

Your team should practice your presentation prior to the final presentation day. This is typically scheduled by the instructional team. During the practice presentation, the instructional team will provide constructive feedback about the flow of the presentation and appearance of the application.

_Why:_
> If there are any issues in your final product's functionality or appearance, it is better to catch them ahead of time. This is also an opportunity to view the application as it will be shared with the audience. Evaluate any screen size issues, color changes due if you are projecting, and overall impact on the user's experience. The practice round will also allow the team to work on the flow of the presentation as speaking roles are passed from one member to another.

Decide whose computer to use during the presentation and have that computer fully ready for practice session. Make sure you have any cables or adaptors needed, and know what settings are needed to share your screen (and audio, if relevant). Test this computer as the driver of the presentation BEFORE your practice. Test a backup computer as well, just in case.

The presentation should follow exactly from the [template slide deck](https://docs.google.com/presentation/d/1jmnVceamFG8mUcP_7zaE06Ai_Jpv2nw6Io5my9m9-i0/){:target="_blank"}. Ensure your timing is no more than 15 minutes long, including some time at the end for questions. Present from the final product, deployed site, or offical documentation that you produce. Each member should introduce themselves with their personal pitch. The "About Us" page provides a great backdrop for this portion of the presentation.

Each member of the team must have a speaking part. It is okay to use note cards if you are nervous about forgetting what to talk about. Some of the areas to discuss include:

* An introduction of the project and the problem domain, including the team's solution
* A demonstration of the final product: highlight your organization, functionality, and all deliverables from the requirements
* The team's approach to planning and communication throughout the project
* A technical obstacle or two and how those obstacles were overcome
* A portion of the final application that each team member is particularly proud of

The appropriate dress code is business casual - not too formal and not too casual.

In addition to the scheduled practice session, the team is encouraged to continue to practice on their own. Keep track of the time and adjust accordingly. Practice with the microphone (muting / unmuting, or holding something if in-person) to feel comfortable with it, and practice passing the microphone between team members as you switch speaking roles if in-person.

Speak clearly and do not use slang or profanity. Take it seriously and be professional.

## Grading

Each team member's grade is split between their individual effort, and the project's technical merit.

Individual effort is graded based on contributions to project deliverables, and professionalism in the presentation.

Technical merit of the project overall is evaluated according the requirements.

## Guideline Requirements

Customized image based OS install:
  - Preconfigure the OS to your liking:
    - Remove bloatware, unnecessary applications
    - Optimize boot time
    - Include applications useful to your clients
  - Create an ISO image and use it to set up an new endpoint
  - Stretch Goal: implement a PXE network boot solution for managing images and provisioning new OSs


User provisioning:
  - Setup a single endpoint as you would for a new user
    - This should include connecting the new user to whatever network or cloud resources they will use (shared folders, backup systems, email address connected to email client, etc.)
  - Use any available tooling to minimize MSP labor in this process
    - Stretch Goal: partially or fully automate this process (imagine entering only the new user's name and email into a script and then letting the setup take care of itself)


Backup Solution:
  - User endpoints will need a backup solution
  - Backups should:
    - Preserve user data
    - Minimize user downtime in the event of system failure


OS Diversity:
  - Your project should include both Windows and Linux systems
  - What role they serve (user endpoint, server, etc.) is up to you


Collaboration:
  - Each user endpoint needs an email client
    - Email client should be connected to the user's email
    - Select and email provider appropriate for the company's needs
      - Assume that the company will have its own domain name, and that the email provider will be providing the backend
      - Create an example account on that provider for demonstration purposes
  - Shared files
    - Users need to be able to collaborate by sharing files and documents
    - Choose and implement an appropriate solution for this need


Remote Access:
  - You will need to establish technology and protocols for secure remote access.
  - You (the MSP) will need remote Admin/root access for management and troubleshooting.
  - Depending on the scenario, users may also need remote access on occasion. Evaluate the client's needs and implement an appropriate solution.
  - Stretch Goal: implement a solution for remotely accessing a user's system over the internet to help them troubleshoot a problem. Assume that the MSP must securely access the machine over the internet.

## Scenario

Your team is a "Managed Service Provider" (MSP) and has been selected as one of the top companies to be contracted as a company's sole IT support, but you still need to win over the client as to why you're the best choice of MSP to work with. The role of client company will be played by your instructor, who will provide you with a fictional scenario consisting of a business, a business objective, required OS, and required software applications.

Your prospective customer is a very small organization (think 5-20 tech-using employees). Until now they have gotten by on off-the-shelf consumer hardware and software solutions, and have no IT policy. Individuals have generally used personal computers, storage, email accounts, etc. The company has purchased some hardware when needed, but these devices are not inventoried or managed by the company.

Now the organization is expanding

If the organization has a payment processing or point-of-sale system, that is already in working order and not part of this project.

Things to consider:
- Does the customer handle sensitive information
  - Is this customer PII?
  - Is this proprietary data, either collected data or intellectual property?
  - Etc.

Your job is to prepare a technical demonstration of how you will meet the given requirements to help the client achieve its business objective.

## Presentation

Components of the presentation must include:

* Introduce your MSP by name, and team members.
* Describe the "Problem Domain" that your instructor provided, including business objectives and any OS or software required.

* Present live technical demonstrations
  * All team members must present an equal share of the live technical demonstrations.
  * The presentation consists of a full provisioning demonstration of a computer system, as well as key operations.
    * A. OS provisioning
      * A1. Demonstrate tool-based provisioning of the required OS.
        * You may not demonstrate standard OEM deployment procedures, but must incorporate a new tool of your choosing into the OS provisioning procedure. Examples of such a tool for Windows include [Windows Autopilot](https://docs.microsoft.com/en-us/mem/autopilot/), [Microsoft Deployment Toolkit](https://www.microsoft.com/en-us/download/details.aspx?id=54259), and [PXE Boot](https://docs.microsoft.com/en-us/troubleshoot/mem/configmgr/understand-pxe-boot). Ideas for Linux can be found on [7 Best Free Linux Server Provisioning Tools](https://www.linuxlinks.com/serverprovisioning/) or you might also consider [PXE Boot](https://docs.microsoft.com/en-us/troubleshoot/mem/configmgr/understand-pxe-boot).
        * Skip processes that take a long time to complete. Remember, your demo time is limited.
    * B. System operations
      * B1. Demonstrate user provisioning of a single end-user (non-administrator account).
      * B2. Demonstrate how remote connectivity will be established to the system by both your MSP and its end user.
        * The end user must have remote access to a user profile with the correct level of permissions (non-administrator). Your MSP must also have remote access to a user profile, however the MSP's will have administrator permissions.
      * B3. Demonstrate how the most important software application will be provisioned and supported by the MSP.
      * B4. Demonstrate a single file or folder data backup and restoration procedure.
        * How will your MSP mitigate the risk of data loss on this new computer system? Your presentation should mention as well how you would perform a baremetal restoration if the OS were to be rendered inoperable.
    * C. Task automation
      * C1. The presentation must include a live technical demonstration of a shell scripting solution that automates repetitive or tedious processes.
        * The team must create and submit at minimum one complete, working, and tested shell script.

## Deliverables

Submit to instructor a single MSP Statement of Work including below deliverables. The document must be submitted as a Google Doc, with a complete version history showing how it was created. All team members are to contribute an equal share to the MSP Statement of Work document and should clearly indicate which components each contributed to in their individual project submission notes.

* GitHub Repository
  * A repo under an appropriately name Github "Organization"
  * Sufficient documentation in the top level README to explain to a stranger who you are, what this project was about, and how all of the material in the repo pertains to it.
    * This README should be:
      * Attractively formatted
      * Include links to relevant files in the repo
      * Include links to each of your own Github accounts AND LinkedIn accounts
  * All other deliverables should be included as files in this repo
* Standard Operating Procedures (SOP)
  * Compose thorough SOPs for each of the following:
    * How will you backup and restore user data, critical infrastructure configurations and hosted data?
    * How will you securely dispose of sensitive data from storage media?
    * How will you perform the support engagements/interactions?
    * What troubleshooting methodology will your technicians follow during support engagements?
    * How will user or department technology purchase requests be handled?
    * How will technology needs be handled for employees being onboarded?
    * How will technology needs be handled for employees being terminated?
    * How will remote, offsite support engagements take place?
    * How will you secure Windows 10 endpoint workstations from data loss and malware threats?
    * How will you administer and support Windows systems?
    * How will your company enhance the network’s usability and security?
    * How will you support company cloud services?
  * For **each** SOP included in your MSP SOW deliverable, attribute authorship to the team member.
  * SOPs can either be:
    * Worked on as google docs and submitted as PDFs
    * Worked on and submitted as Markdown files
  * Systems Documentation
    * Include in your deliverable any relevant information required for the operation of the demonstrated system.
      * Any config files which you created or customized, exported in an appropriate format (such as json)
    * Network Topology
* Presentation Material
  * Slide deck, as a PDF
  * A link to the video of your presentation (when it becomes available)
* Stretch Goal: Service Level Agreement (SLA)
  * Compose a complete, original, branded Service Level Agreement clearly indicating service delivery times and scope of services supported.
  * Should be worked on as a google doc and submitted as a PDF.
