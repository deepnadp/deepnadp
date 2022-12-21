- DELETE /clients/:id

 

The response status should be 204.

 

------------------------------------------------------------

 

Create a new project

POST clients/:id/projects/

 

Here you do not need to create any new user but assign already registered users.

retrieve client id from the url and assign it to a project.

 

Input = {

	'project_name' : 'Project A'

	'users' : [

    		{

        			'id' : 1,

        			'name' : 'Rohit'

    		}

	]

}

 

Output = {

        	 	'id' : 3,

        		'project_name' : 'Project A',

	    	'client' : 'Nimap'

	    	'users' :         	[

    	            		{

        	                                	'id' : 1,

        	                                	'name' : 'Rohit'

    	            		}

	    	]

	    	'created_at' : '2019-12-24T11:03:55.931739+05:30'

	    	'created_by' : 'Ganesh'

}

 

-------------------------------------------------------------

 

 

List of all projects assigned to the logged-in user

GET /projects/

[

	{

   	 	'id' : 1,

    		'project_name' : 'Project A',

   	 	'created_at' : '2019-12-24T11:03:55.931739+05:30',

   	 	'created_by' : 'Ganesh'

	},

	{
