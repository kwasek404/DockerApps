node('charger') {
	echo "Cleaning cache"
	sh "docker system prune -a -f"
	def images = ["template-fedora", "template-ubuntu", "docker-darktable", "docker-dbeaver", "docker-firefox", "docker-jenkins", "docker-libreoffice", "docker-spotify", "docker-tor"]
	for (image in images) {
		buildImage(image)
	}
}

def buildImage(imageName) {
	stage(imageName) {
		steps {
			echo "Building ${imageName}"
			sh "./build ${imageName}"
		}
	}
}
