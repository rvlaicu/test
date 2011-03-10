================================================================================
How to Use Review Board
================================================================================

Every MarkUs developer has to use Review Board (even for the smallest commit).
[[Review Board | http://review.markusproject.org]] is our tool for
peer-reviewing to-be-checked-in source code. This is a short guide as to how
to use Review Board.

Creating New Review Requests
================================================================================

Once you have changed the source code of your locally checked out copy of
MarkUs you need to create a new review request for these changes. This are the
steps you need to do:

 1. Create a diff file for your changes made (Do _not_ include files in the
 diff file, which you do not plan to commit to the MarkUs source code
 repository). Usually one would use svn diff and redirect output to a file.

 2. Go to <http://review.markusproject.org/> and log in with your credentials
 (If you do not have a Review Board account, request one from the
 administrator)

 2. Click on "New Review Request"

    223. Enter "Base Diff Path" (this is the directory - inside the MarkUs
    source code repository - you checked out **plus** possibly some
    sub-folders inside the MarkUs app you created the diff in). For instance,
    if you have checked out the "trunk" directory of the MarkUs code base and
    you created the diff by running <code>svn diff \> out.diff</code> in the
    application root directory, you should enter "trunk" as a "Base Diff
    Path". You can find out what folders there are in the MarkUs source code
    repository by [browsing the source code
    online](https://stanley.cdf.toronto.edu/svn/csc49x/olm_rails/)

    232. Upload the diff you created in step 1

 4. Check the diff by clicking on "View Diff"

 3. Enter appropriate "Summary" and "Description"

 3. If this is a review request for a particular branch enter the branch name in "Branch"

 3. If this review request addresses a particular bug for which there exists a ticket enter ticket number in "Bugs"

 3. If you want to get review of any MarkUs developer, enter
    "markus_developers" in field "Groups". If you want to get review by one
    particular MarkUs developer you enter the Review Board username of that
    developer in field "People". *Note:* Groups and People are auto-completing
    fields, which might be handy sometimes.

 2. Once you are satisfied with your review request, you need to **publish**
    it in order to have review-request-emails sent out.

 3. You may also choose to let your peer developers know about the new
   review-request in the MarkUs IRC channel.


Reviewing Code of Your Peer-Developers
--------------------------------------------------------------------------------

In general, after a review-request has been uploaded, there are 3 steps code,
topic of a review-request, has to go through before it gets checked in into
the MarkUs source code repository: 1. comment review-request 2. revise
review-request (if need be) and 3. check in changed source code (_provided_
the review-request got a green light - i.e. a "ship it"). Step one and two
need be repeated as appropriate and until the review-request gets a "ship it"
(or gets dropped without being committed at all).

But how to comment review-requests? How do you give a "ship it"? The following
steps outline how to do these things:

 1. Go to <http://review.markusproject.org/> and log in with your credentials

 2. Let other developers know that you are about to review review-request X,
    in order to avoid conflicts

 2. Select review-request (from the dashboard) you would like to review and
    click on it

 3. Once you have the desired review-request open, click on "View Diff"

 2. Comment code by clicking on appropriate line numbers on the right or in
    the middle (In order to delete comments click green clip on the very right
    to open the comment again; then click the "Delete" button)

 2. Once you are done commenting code of the review-request, **publish** your
    comments. You should _not_ check "ship it", if you expect your
    peer-developer to revise the review-request!

 3. Optionally let your peer-developer know that you have reviewed his/her
   code.

 3. If you think code is ready to be committed, give a "ship it" by clicking
   "Review" or "Edit Review".