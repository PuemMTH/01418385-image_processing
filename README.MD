# Image Processing
```
FUNCTION COUNTPIXELS (IMAGE: Array(X,Y,COLOR)):
	A = IMAGE
	FOR i = (0,0) TO (N,N2):
		X = N
		Y = N2
		IF ((X,Y) == (X,Y)):
			APPEND (X,Y) TO A
	CATCH = Array(X,Y,COLOR)[1]
	FOR A[0] TO A[N]:
		IF (A[i] == 0):
			IF A[i+1] == 0:
				APPEND A[i] TO CARCH[0]
			IF A[i-1] == 1:
				APPEND A[i] TO CARCH[0]
	COUNT = 0
	FOR CATCH[0] TO CATCH[N]:
		COUNT = COUNT + 1
	RETURN COUNT
```

# Count Pixels in image
```
FUNCTION LINECOUNT (IMAGE: Array(X,Y,COLOR)):
	Y = IMAGE.COPY(COLUMN[0])/2 -> INT
	POINT_A = X,Y,COLOR
	POINT_B = X,Y,COLOR
	FOR IMAGE(Y, 0) TO IMAGE(Y, N):
		IF IMAGE(Y, i) == 0:
			SET IMAGE(Y, i) TO POINT_A
		ELSE:
			SET IMAGE(Y, i) TO POINT_B
	
	COUNT = 0
	FOR IMAGE(A.Y, 0) TO IMAGE(A.Y, N):
		COUNT = COUNT + 1

	LINE_A, LINE_B = 0, 0
	FOR IMAGE(X, 0) TO LINE_A, IMAGE(X, 0) TO LINE_B:
		IF IMAGE(X, i) == POINT_A:
			IF LINE_A(X, i) == 0:
				LINE_A = LINE_A + 1
		IF IMAGE(X, i) == POINT_B:
				IF LINE_A(X, i) == 0:
					LINE_B = LINE_B + 1

	RETURN COUNT, LINE_A, LINE_B
```

# Count Lines in image
```
FUNCTION CONTAINCOLOR (IMAGE: Array(X,Y,COLOR)):
	IMAGE_X = X/2
	IMAGE_Y = Y/2

	FIND_COLOR = GET IMAGE(IMAGE_X, IMAGE_Y)
	RETURN COLOR = FIND_COLOR
```