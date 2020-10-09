node('awsnode')
{
stage ('scm')
{
git 'https://github.com/Vamshi270991/game-of-life.git'
}
stage('build')
{
sh 'mvn package'
}
stage('post build')
{
archiveArtifacts artifacts: 'gameoflife-web/target/*.war', followSymlinks: false
junit 'gameoflife-web/target/surefire-reports/*.xml'
}
}
