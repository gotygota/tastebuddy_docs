# User administration

Users are to be understood as the tasters or assessors. They will be able to use
the predefined protocols to analyse product, either during tasting sessions or
as punctual tastings. They can have two roles:

1. **Regular user**: can access all the tasting sheets available, conduct
   punctual tasting (and therefore add their own products) and be assigned
   tasting sessions. The cannot create their own tasting protocols nor modified any
   existing ones, and can only view the details of products they created during
   punctual tastings. A regular user can only view their own results (all other
   being anonymized).
2. **Administrator**: on top of all Regular User's permissions, Administrators can
   create criteria, tasting sheets, tasting sessions, as well as products. They
   can modify any existing record, whether created by them or any other user.
   They can view all unanonymized results of regular users and products.

The following sections consider the user has administrator access.

## Adding users

New users can be added to your organisation by sending them a unique link to
create an account.

Go to [https://tastebuddy.io/users/](https://tastebuddy.io/users/) or click in
`Users` in the left sidebar. In the `ADD USERS` section, fill in the email
address of the user you wish to invite, then click on send (*one address at a
time*). The system will send a link to the indicated email address the user can
follow to create their account and connect to the organisation.

![User invitation section](images/user_invite.png#only-light){ loading=lazy }
![User invitation section](images/user_invite_dark.png#only-dark){ loading=lazy }

!!! warning "Invitations will expire"
    The invitation sent to the email address contains a link which will expire
    after 3 days. In case the expiration date has been passed, you can resend an
    invitation to the user by clicking on the button next to their name at the
    bottom of the same page.

    Trying to resend an invitation to an existing user or the an email with a
    pending invitation will trigger an error. In case the email hasn't been
    received, use the bottom table displaying the pending and expired invitation in
    order to send a new link.

    ![Invitation status section](images/user_invite_2.png#only-light){ loading=lazy }
    ![Invitation status section](images/user_invite_2_dark.png#only-dark){ loading=lazy }

## Updating a user's profile

You can quickly edit a user's profile by clicking on `Edit` in the users table.
However, only the users themselves can update their own password and email
address, by accessing their profile at
[https://tastebuddy.io/users/update/](https://tastebuddy.io/users/update/)

!!! tip "About personal information"
    It is strongly recommended to fill in the personal information of the users
    and encourage them to do so, as it can provide valuable information regarding
    a taster sensitivity and consumers profiling in the long run
## User's deletion

As a user can have provided useful information from sensory evaluation, their
access can be revoked instead of purely deleting their accounts. A deactivated
users will not be able to access any of the Tastebuddy pages. A deactivated
account can also be reactivated without loss of any kind of data.

You can revoke (respectively reopen) a user access to the platform by simply
clicking on Deactivate (respectively Reactivate) from the users table. To do so,
click on `deactivate`. 

!!! danger "Actually deleting an account"
    Results associated to a deactivated account will still show up in
    dashboards. In case you consider the results to not be useful anymore, the
    account can be deleted. All results associated with the account will also be
    deleted. **BE CAREFULL: SUCH ACTION IS IRREVOCABLE**
