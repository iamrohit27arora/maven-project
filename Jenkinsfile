pipeline{

agent any

stages{

stage ('scm checkout'){

steps {

git branch: 'master', url: 'https://github.com/iamrohit27arora/maven-project.git'

}

}

stage ('compile the code'){

steps {

withMaven(jdk: 'EC2JDK', maven: 'EC2Maven') {
    sh 'mvn compile'
}

}

}
    
    stage ('test the code'){

steps {

withMaven(jdk: 'EC2JDK', maven: 'EC2Maven') {
    sh 'mvn test'
}

}

}
    
     stage ('package the code'){

steps {

withMaven(jdk: 'EC2JDK', maven: 'EC2Maven') {
    sh 'mvn package'
}

}

}

}

}


