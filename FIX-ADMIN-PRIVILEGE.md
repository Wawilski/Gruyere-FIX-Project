
# Exploit description

Any user could set himself or some other user as admin, using the URL extension :

```
/saveprofile?action=update&is_admin=True&uid=user_uid
```

The same exploit could be used to create a new admin user, using the URLextension :

```
/saveprofile?action=new&is_admin=True&is_author=True&uid=user_uid&pwd=user_pwd
```

# Exploit source

In the source code, the function managing profiles changes doesn't verify the request permissions before actually doing it.

So we could easily add anything relative the privileges of a user in the URL, and the request would be executed.

# Exploit Fix

Adding a verification when the URL is received, if the user is an admin, then they can modify the privileges, they can't in the other way


