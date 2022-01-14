# Workshop with a single set of labs

## Instructions - Delete this file when finished

1. Open the workshop-single-sets template in Atom or Visual Studio Code using workshop-single
2. Start atom-live-server (Atom) or live-server (Visual Studio Code)
3. We precreated 7 folders.  A workshop is created out of multiple labs.  
4. Make sure you stick to all lower case and dashes for spaces
5. Your image names should have descriptive names. Not just adb1, adb2, adb3.  For handicap accessiblity we need the image descriptions to explain what the image looks like.  Remember all lower case and dashes.
6. Make sure you watch this [video](https://otube.oracle.com/media/1_ucr6grc6) for how to do Self QA of a workshop.  These are the standards that need to be met before going to production.  (It's short don't worry!)
7. Download our [QA Feedback doc](https://confluence.oraclecorp.com/confluence/download/attachments/1966947336/LiveLabs-QA-Feedback-Form-v2.docx?version=2&modificationDate=1598913736000&api=v2) as well.  We find workshops get in production quicker when you know what's needed to move to production up front and you use the skeleton.

PS  You do not need a Readme.md.  Readme's exist only at the top library levels. We direct all traffic to LiveLabs since we can't track usage on GitHub.  Do not create any direct links to GitHub, your workshop may be super popular but we can't track it so no one will know.


## Folder Structure

In this example, the goal is to create several "children" workshops from one longer "parent" workshop. The children are made up of parts from the parent.

sample-workshop/
        -- individual labs

        provision/
        setup/
        dataload/
        query/
        analyze/
        visualize
        introduction/
          introduction.md       -- description of the everything workshop, note that it is a "lab" since there is only one

    workshops/
       freetier/                -- freetier version of the workshop
        index.html
        manifest.json
       livelabs/                -- livelabs version of the workshop
        index.html
        manifest.json


### FreeTier vs LiveLabs

* "FreeTier" - includes Free Trials, Paid Accounts and for some workshops, Always Free accounts (brown button)
* "LiveLabs" - these are workshops that use Oracle provided tenancies (green button)

### About the Workshop

The workshop includes all 6 of the individual labs in a single sequence.

The folder structure includes a Introduction "lab" that describes the workshop as a complete set of 6 labs. Note: you may not need to have a different introduction for each of the parent and child versions of the workshops, this is illustrative only.

Look at the product-name-workshop/freetier folder and look at the manifest.json file to see the structure.

The Prerequisite "lab" is the first lab in a common folder on the oracle/learning-library repo. Because this lab already exists, we can use a RAW/absolute URL instead:

  ```
  "filename": "https://raw.githubusercontent.com/oracle/learning-library/master/common/labs/cloud-login/cloud-login-livelabs2.md"        },
  ```

The manifest.json file needs to know the location of each lab relative to where it exists in the hierarchy. In this structure, labs are located two levels up, for example:

  ```
  "filename": "../../provision/provision.md"
  ```

### For example:

This [APEX Workshop](https://oracle.github.io/learning-library/developer-library/apex/spreadsheet/workshops/freetier/) is a good example a workshop with a single set of labs: [https://github.com/oracle/learning-library/tree/master/developer-library/apex/spreadsheet](https://github.com/oracle/learning-library/tree/master/developer-library/apex/spreadsheet).


### More information

* [Creating the Structure of Markdown Labs](https://confluence.oraclecorp.com/confluence/display/DCS/Creating+the+Structure+of+Markdown+Labs)
* [See a working example on GitHub](https://github.com/oracle/learning-library/tree/master/data-management-library/autonomous-database/shared)

## Adding Support Forum

Copy the following section.  Replace the general support link with the support link for your workshop category.  We have a number of pre-created forums, click edit on your workshop to see if your workshop fits into any of the existing forums.  If not, submit a comment on your workshop to request to have one added.   Go back to the [LWMS](bit.ly/oraclelivelabs), Edit your workshop and see if a support forum exists for your workshop already (or if you have a forum you want to use, email us, we will add it to the list).  

