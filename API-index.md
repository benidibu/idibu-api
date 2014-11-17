### **Overview of the Adpost XML v3 API**

Adpost XML v3 allows third parties to access the idibu posting engine by posting XML to the system.

Our Adpost XML API V3 builds on top of our previous versions to provide more intelligence in the back-end. In addition to the previous 2 methods

- ADD
- UPDATE
- REPOST
- QUICKREPOST
- DELETE
- CANCEL

that allows not only for complete management of your job posting, but allows excellent flexibility when it comes to the XML data package that you send.

Depending on the method employed - the API implements what we call the "Posting Completion Page", a page accessed through a secure URL, where the consultant can complete the posting process by filling the data that was missing from the initial posting, IF our system finds that the XML data package is missing critical data - or the remote system forces this page. It uses the same business intelligence that drives idibu to map the data sent to the different board requirements.

The "Posting Completion Page" (PCP) is a regular web page where users provide any additional information required to complete a post and is:

- So simple that no training is required
- Designed to be completely re-branded and customized for partners including:
1. the posting url, allowing for fully brand-embedded posting to be integrated into third party systems.
2. the email box used for notifications, that can be configured so any standard SMTP email account can be used

Besides the previous set of XML tags, we have added a new set to deal with how the PCP will be handled, plus the use of a client reference tag that makes it possible to integrate idibu's two main products, AdPost and ApTrack into the client system in a much tighter way - and what we call "dynamic core fields", a concept that simplifies sending duplicated data to the different boards in a centralized way.
API XML blocks

The xml payload used to post to idibu split into 5 blocks of data, where 3 of them relates to the job itself and 1 to the boards intended to post. The blocks of data are grouped like this:

    Job data
        PCP configuration data
        Job core fields and dynamic core fields
        Sender and team information
    Board posting information

The description and usage of each group and its tags are explained below, with special emphasis in those tags that we consider more important for the posting process. You can view working examples here.