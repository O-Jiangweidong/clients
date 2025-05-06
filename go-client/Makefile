NAME=go-client
BUILDDIR=build

BASEPATH := $(shell pwd)
CLIENTSRCFILE := $(BASEPATH)/cmd/awaken/
SSHCSRCFILE := $(BASEPATH)/cmd/sshc/

LDFLAGS=-w -s

CLIENTBUILD=CGO_ENABLED=0 go build -trimpath

build-client:
	GOARCH=amd64 GOOS=windows $(CLIENTBUILD) -ldflags "$(LDFLAGS) -H windowsgui" -o $(BUILDDIR)/windows/JumpServerClient.exe $(CLIENTSRCFILE)

	cp -R $(BUILDDIR)/* $(BASEPATH)/../interface/bin/
	cp $(BASEPATH)/config.json $(BASEPATH)/../interface/bin/
	cp $(BASEPATH)/putty.exe $(BASEPATH)/../interface/bin/windows/