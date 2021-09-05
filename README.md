# user-sequelize

* Install dependencies with `npm install`
* Run the express server with `npm start`
* Open your browser in `localhost:3000` and try the example REST endpoints.
---
  * User endpoints
	  * `localhost:3000/user` (GET) - get all users
	  * `localhost:3000/user/[someid]` (GET) - get user by id
	  * `localhost:3000/user/post` (POST) - create a user
		  * Body format: `{ name: 'Petr', email: 'petr@gmail.com' }`
	  * `localhost:3000/user/patch` (PATCH) - assign role to user
		  * Body format: `{ userUuid: 'someid', roleUuid: 'someid' }`

---
  * Permission endpoints
	  * `localhost:3000/permission` (GET) - get all permissions
	  * `localhost:3000/permission/post` (POST) - create a permission
		  * Body format: `{ name: 'CREATE' }`
	  * `localhost:3000/permission/delete` (DELETE) - delete a permission by uuid
		  * Body format: `{ permissionUuid: 'someid' }`
---
  * Role endpoints
	  * `localhost:3000/role` (GET) - get all roles
	  * `localhost:3000/role/post` (POST) - create a role
		  * Body format: `{ name: 'Admin', permissionUuids: ['someid1', 'someid2']}`
	  * `localhost:3000/role/patch` (PATCH) - add new permission to role
		  * Body format: `{ permissionUuid: 'someid', roleUuid: 'someid' }`
