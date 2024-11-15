# Jenkins-testing
Jenkins pipeline starchers
===========================
[Refer Here ](https://www.jenkins.io/doc/book/pipeline/syntax/) Jekins pipeline starchers 

 sections 
----------
	1. agent -> 
		* any
		* none 
		* label
		* node 
	2. post 
 		* always
		* changed 
		* fixed
		* regression 
		* aborted
		* failure 
		* success
		* unstable
		* unsuccessful
		* clean-up
	3. stages
		* steps 
	4. environment  
		* secret text
		* secret file
		* username and passwd
		* ssh with private key
			call the -- > Name = credentials()
	5. options 
		* retry
		* skipStagesAfterUnstable 
		* skipDefaultCheckout
		* timeout 
	6. parameters
		* string
		* text
		* booleanParam
		* choice 
		* password 
	7. triggers
		* cron
		* pollSCM
		* upstream 
	8. tools  
	9. input --> this section is used for allowing user approval 
		* message
		* id 
		* ok 
		* submitter  -- name of user
		* submitterParameter
		* parameters 
	10. when 
		* branch
		* buildingTag
		* environment 
		* tag 
		* not --> execute the nested condition is false 
		* allof --> Execute the stage when all of the nested conditions are true.
		* anyOf --> Execute the stage when at least one of the nested conditions is true. 

		* triggeredBy 
		* 
	11. parallel 
	12. sequential Stages 

===============

scenario-->
------------
 2. In declarative pipeline in 5 stages if stage 2 failed then it should continue to next, not to failed.

	catchError(buildResult: 'SUCCESS', stageResult: 'UNSTABLE')

3. How to check current stage?
