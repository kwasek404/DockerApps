node('charger') {
	def images = ["template-fedora", "template-ubuntu", "docker-darktable", "docker-dbeaver", "docker-firefox", "docker-jenkins", "docker-libreoffice", "docker-spotify", "docker-tor"]
	stage("Cloning git repo") {
		echo "Cloning repo"
		git(url: 'https://github.com/kwasek404/DockerApps.git')
	}
	stage("Cleaning cache") {
		echo "Cleaning cache"
		sh "docker system prune -a -f"
	}
	for (image in images) {
		buildImage(image)
	}
}

def buildImage(imageName) {
	stage(imageName) {
		echo "Building ${imageName}"
		sh "./build ${imageName}"
	}
}
