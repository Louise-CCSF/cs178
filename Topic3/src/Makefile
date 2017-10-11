HOME=..
BUILD=build
DATA=data
SOURCE=src

default: test 

readInt32BitLE: readInt32BitLE.c
	cc -c readInt32BitLE.c -o readInt32BitLE 

CountThrees: ServerCountThrees.c
	cc -c ServerCountThrees.c -o CountThrees

ServerCountThrees: readInt32BitLE CountThrees
	cc -o ServerCountThrees readInt32BitLE CountThrees

clean: 
	rm -rf readInt32BitLE CountThrees ServerCountThrees ${HOME}/${BUILD}

test: ServerCountThrees
	mkdir ${HOME}/${BUILD}
	cp ${HOME}/${DATA}/threesData.bin ${HOME}/${BUILD}/
	cp ${HOME}/${SOURCE}/ServerCountThrees ${HOME}/${BUILD}/
	cd ${HOME}/${BUILD}
	./ServerCountThrees
