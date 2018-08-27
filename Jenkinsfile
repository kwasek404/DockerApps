node('charger') {
	def images = ["template-fedora", "template-ubuntu", "docker-darktable", "docker-dbeaver", "docker-firefox", "docker-jenkins", "docker-libreoffice", "docker-spotify", "docker-tor"]
	for (image in images) {
		buildImage(image)
	}
}

def buildImage(imageName) {
	echo "Building ${imageName}"
}
