T3_HOME=/home/louise/Topic3
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
	rm -rf readInt32BitLE CountThrees ServerCountThrees ${T3_HOME}/${BUILD}

test: ServerCountThrees
	mkdir ${T3_HOME}/${BUILD}
	cp ${T3_HOME}/${DATA}/threesData.bin ${T3_HOME}/${BUILD}/
	cp ${T3_HOME}/${SOURCE}/ServerCountThrees ${T3_HOME}/${BUILD}/
	cd ${T3_HOME}/${BUILD}
	./ServerCountThrees
