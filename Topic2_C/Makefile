Count3s: 
	cc -c readInt32BitLE.c -o readInt32BitLE 
	cc -c CountThrees.c -o CountThreesC
	cc -o Count3s readInt32BitLE CountThreesC

runCount3s: Count3s
	./Count3s

clean: 
	rm -f Count3s readInt32BitLE CountThreesC
