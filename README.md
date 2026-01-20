plugins {
    id 'java'
}

group = 'com.yourserver'
version = '1.0.0'

java {
    toolchain.languageVersion = JavaLanguageVersion.of(17)
}

repositories {
    mavenCentral()
    maven { url = 'https://maven.minecraftforge.net/' }
}

dependencies {
    minecraft 'net.minecraftforge:forge:1.20.1-47.1.0'
}

minecraft {
    mappings channel: 'official', version: '1.20.1'
    runs {
        server {
            workingDirectory project.file('run')
            args '--nogui'
        }
    }
}
