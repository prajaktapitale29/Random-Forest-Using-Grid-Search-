# Random-Forest-Using-Grid-Search-
Identified the factors that predict user adoption using Random Forest for a small business

A user table ("takehome_users") with data on 12,000 users who signed up for the product in the last two years. This table includes: 

    name: the user's name
    object_id: the user's id
    email: email address 
    email_domain: domain of email address, e.g. gmail.com
    creation_source: how they signed up for the product. This takes on one of 5 values:
        PERSONAL_PROJECTS: invited to join another user's personal workspace
        GUEST_INVITE: invited to an organization as a guest (limited permissions)
        ORG_INVITE: invited to an organization (as a full member)
        SIGNUP: signed up via myapp.com
        SIGNUP_GOOGLE_AUTH: signed up using Google Authentication (using a Google email account for their login id) 
    creation_time: when they created their account
    last_session_creation_time: unix timestamp of last login
    opted_in_to_mailing_list: whether they have opted into receiving marketing emails
    enabled_for_marketing_drip: whether they are on the regular marketing email drip
    org_id: the organization (group of users) they belong to
    invited_by_user_id: which user invited them to join (if applicable). 

 
A usage summary table ("takehome_user_engagement") that has a row for each day that a user logged into the product.  
 
We define an "adopted user" as a user who has logged into the product on three separate days in at least one seven-day period. Because we believe that adopted users are more likely to be successful at using myapp in the long term than those that are not adopted, we want to know what things are likely indicators of future adoption. With this in mind, we'd like to identify which factors predict user adoption.
