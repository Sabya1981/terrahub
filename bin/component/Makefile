BINARY=component
GOARCH32=386
GOARCH64=amd64
VERSION=v0.0.1

all: linux solaris darwin windows vet fmt fmtcheck errcheck golint

linux:
	@echo
	@rm ../linux_${GOARCH32}/${BINARY} && echo 'LINUX BINARY FOR i386 ARCHITECTUR REMOVED SUCCESFULLY' || echo 'LINUX BINARY FOR i386 ARCHITECTUR WERE NOT REMOVED'
	@echo 'BUILDING LINUX BINARY FOR i386 ARCHITECTURE'
	@GOOS=linux GOARCH=${GOARCH32} go build -o ../linux_${GOARCH32}/${BINARY} \
	-ldflags="-X main.Version=${VERSION}" &&  \
		echo 'BUILD EXECUTED SUCCESSFULLY' || echo 'BUILD FAILED'

	@rm ../linux_${GOARCH64}/${BINARY} && echo 'LINUX BINARY FOR amd64 ARCHITECTUR REMOVED SUCCESFULLY' || echo 'LINUX BINARY FOR amd64 ARCHITECTUR WERE NOT REMOVED'
	@echo 'BUILDING LINUX BINARY FOR amd64 ARCHITECTURE'
	@GOOS=linux GOARCH=${GOARCH64} go build -o ../linux_${GOARCH64}/${BINARY} \
	-ldflags="-X main.Version=${VERSION}" &&  \
        echo 'BUILD EXECUTED SUCCESSFULLY' || echo 'BUILD FAILED'

solaris:
	@echo
	@rm ../solaris_${GOARCH64}/${BINARY} && echo 'DARWIN BINARY FOR amd64 ARCHITECTUR REMOVED SUCCESFULLY' || echo 'DARWIN BINARY FOR amd64 ARCHITECTUR WERE NOT REMOVED'
	@echo 'BUILDING DARWIN BINARY FOR amd64 ARCHITECTURE'
	@GOOS=darwin GOARCH=${GOARCH64} go build -o ../solaris_${GOARCH64}/${BINARY} \
	-ldflags="-X main.Version=${VERSION}" &&  \
        echo 'BUILD EXECUTED SUCCESSFULLY' || echo 'BUILD FAILED'
	
darwin:
	@echo
	@rm ../darwin_${GOARCH64}/${BINARY} && echo 'DARWIN BINARY FOR amd64 ARCHITECTUR REMOVED SUCCESFULLY' || echo 'DARWIN BINARY FOR amd64 ARCHITECTUR WERE NOT REMOVED'
	@echo 'BUILDING DARWIN BINARY FOR amd64 ARCHITECTURE'
	@GOOS=darwin GOARCH=${GOARCH64} go build -o ../darwin_${GOARCH64}/${BINARY} \
	-ldflags="-X main.Version=${VERSION}" &&  \
        echo 'BUILD EXECUTED SUCCESSFULLY' || echo 'BUILD FAILED'

windows:
	@echo
	@rm ../windows_${GOARCH32}/${BINARY} && echo 'WINDOWS BINARY FOR i386 ARCHITECTUR REMOVED SUCCESFULLY' || echo 'WINDOWS BINARY FOR i386 ARCHITECTUR WERE NOT REMOVED'
	@echo 'BUILDING WINDOWS BINARY FOR i386 ARCHITECTURE'
	@GOOS=windows GOARCH=${GOARCH32} go build -o ../windows_${GOARCH32}/${BINARY} \
	-ldflags="-X main.Version=${VERSION}" &&  \
        echo 'BUILD EXECUTED SUCCESSFULLY' || echo 'BUILD FAILED'

	@rm ../windows_${GOARCH64}/${BINARY} && echo 'WINDOWS BINARY FOR amd64 ARCHITECTUR REMOVED SUCCESFULLY' || echo 'WINDOWS BINARY FOR amd64 ARCHITECTUR WERE NOT REMOVED'
	@echo 'BUILDING WINDOWS BINARY FOR amd64 ARCHITECTURE'
	@GOOS=windows GOARCH=${GOARCH64} go build -o ../windows_${GOARCH64}/${BINARY} \
	-ldflags="-X main.Version=${VERSION}" &&  \
        echo 'BUILD EXECUTED SUCCESSFULLY' || echo 'BUILD FAILED'

.PHONY: linux solaris darwin windows
