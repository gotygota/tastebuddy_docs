# User administration

First builiding block of Tastebuddy, the users are the tasters or assessors.
They will be able to use the pre-defined protocols to analyze the product,
either during tasting sessions or as punctual tastings.

## About roles

There are two main types of users:

1. **Regular user**: has access to all available tasting sheets, can perform
   punctual tastings (and thus add their own products) and be assigned tasting
sessions. They cannot create their own tasting notes or modify existing ones,
and can only view the details of the products they have created during the
punctual tastings. A regular user can only view his own results (all others are
anonymized).
2. **Administrator**: in addition to all the rights of a regular user,
   administrators can create criteria, tasting sheets, tasting sessions and
products. They can modify any existing record, whether created by themselves or
by another user. They can view all non-anonymous results of regular users and
products. Finally, administrators can invite new users, edit their profile, and
promote to administrator role.

There also exists one `SuperUser`, who supersed the administrators and whose
role cannot be changed.

The following sections assume that the user has administrator access.

## Adding users

New users can be added to your organization by sending them a unique link to create an account.

Go to [https://tastebuddy.io/users/](https://tastebuddy.io/users/) or click
`Users` in the left sidebar. In the `ADD USERS` section, enter the email address of
the user you want to invite, then click `Send` (one address at a time). The system
will send a link to the specified email address that the user can follow to
create their account and connect to the organization.

![User invitation section](images/user_invite.png#only-light){ loading=lazy }
![User invitation section](images/user_invite_dark.png#only-dark){ loading=lazy }

!!! warning "Invitations have an expiration date"
    The invitation sent to the email address contains a link that expires after 3
    days. If the expiration date has passed, you can resend an invitation to the
    user by clicking the button next to their name at the bottom of the same page.

    Attempting to resend an invitation to an existing user or an email with a
    pending invitation will result in an error. If the email hasn't been received,
    use the table at the bottom of the page that shows pending and expired
    invitations to send a new link.

    ![Invitation status section](images/user_invite_2.png#only-light){ loading=lazy }
    ![Invitation status section](images/user_invite_2_dark.png#only-dark){ loading=lazy }

## Updating a user's profile

You can quickly edit a user's profile by clicking `Edit` in the Users table.
<figure markdown="span">
![User profile edition](images/user_edit.png#only-light){ loading=lazy }
![User profile edition](images/user_edit_dark.png#only-dark){ loading=lazy }
</figure>

### Personal information
You can easily update a user's first name, last name, date of birth,
nationality, and gender using the quick form. Update all relevant data and click
`Update`.
<figure markdown="span">
    ![User profile edition](images/user_edit_2.png#only-light){ loading=lazy, width="70%" }
    ![User profile edition](images/user_edit_2_dark.png#only-dark){ loading=lazy, width="70%" }
</figure>

!!! tip "About personal information"
    It is strongly recommended that users fill out their personal information,
    as this can provide valuable information about taste sensitivities and consumer
    profiling in the long run. Encourage the users to do so!

### Role

Administrators can promote any regular user to the administrator role by
checking the `Make admin` box. They will automatically get access to all pages and
data of the organization account.

Note that administrators cannot change the role of other administrators to
regular user. The organization's `SuperUser` is the only user who can demote
administrators to regular users.

!!! note "Switching SuperUser"
    To assign the the SuperUser role to a new user, please [contact us](https://tastebuddy.io/contact/).

### Login information

Only users themselves can update their own password and email
address, by accessing their profile at
[https://tastebuddy.io/users/update/](https://tastebuddy.io/users/update/). A
new confirmation email will be sent to the new email address in order to
confirm its validity.

## User's deletion

Since a user may have provided useful sensory information, their access may be
revoked instead of simply deleting their account. A deactivated user will not be
able to access any of the Tastebuddy sites. A deactivated account can also be
reactivated without any loss of data.

You can deactivate (or reactivate) a user's access to the platform by simply
clicking on Deactivate (or Reactivate) in the user's table. To do this, click on
`De/Re-activate`.

!!! danger "Actually deleting an account"
    Results associated with a deactivated account will still appear in dashboards.
    If you decide that the results are no longer useful, you can delete the account.
    All results associated with the account will also be deleted. **BE CAREFULL:
    SUCH ACTION IS IRREVOCABLE**
