# Dashboard App Flow

![](../.gitbook/assets/dashboard-app-flow.png)

An admin can login using his/her email id and password for the mfund-dashboard-app. The email Id and password associated with it would be verified in the backend and an access token will be generated. After logging in admin can view the total number of investors, total investments and total balances on the home page. He/she can also add organisation from home page. Admin can use drawer for navigating to other screens. In investment plan screen , admin can view the details of all the organisations and as well add some organisations. Admin can. Also view the details of all the investors and users who have made transactions. The logged in admin can create a new admin from settings screen and also can change his/her current password. And then he/she can logout by making a post request with firebase JWT token to revoke the refresh token from firebase authentication.

