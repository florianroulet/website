node('dind') {
  // This displays colors using the 'xterm' ansi color map.
  ansiColor('xterm') {
    checkout scm

    sh 'env'
    sh 'pwd'
    sh 'make release'
    sh 'ls -lR'
    archiveArtifacts 'dist'
  }
}