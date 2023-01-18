pipeline
	{
		agent any
		stages{
			stage('Build Application'){
			steps{
				bat 'mvn clean install'
				}
			}
			stage('Deploy Application to Mulesoft CloudHub'){
			steps{
					bat 'mvn package deploy -DmuleDeploy'
				 }
				}
			stage('Perform regression testing'){
			steps{
					bat 'newman run "C:\\Users\\nikhi\\OneDrive\\Desktop\\WorldTimeZone Collection.postman_collection.json" --disable-unicode'
				 }
			  }
	}
}