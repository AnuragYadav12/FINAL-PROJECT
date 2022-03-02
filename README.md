# FINAL-PROJECT
# Python3 program for point clipping Algorithm

# Function for poclipping
def pointClip(XY, n, Xmin, Ymin, Xmax, Ymax):
	for i in range(n):
		if ((XY[i][0] >= Xmin) and
			(XY[i][0] <= Xmax)):
			if ((XY[i][1] >= Ymin) and
				(XY[i][1] <= Ymax)):
				print("[", XY[i][0], ", ", XY[i][1],
					"]", sep = "", end = " ")
		
	# prpocoordinate outside viewing pane
	print("\n\nPoint outside the viewing pane:")
	for i in range(n):	
		if ((XY[i][0] < Xmin) or (XY[i][0] > Xmax)) :
			print("[", XY[i][0], ", ", XY[i][1],
				"]", sep = "", end = " ")
		if ((XY[i][1] < Ymin) or (XY[i][1] > Ymax)) :
			print("[", XY[i][0], ", ", XY[i][1],
				"]", sep = "", end = " ")


if __name__ == '__main__':
	XY = [[10, 10], [-10, 10], [400, 100],
		[100, 400], [400, 400], [100, 40]]

	
	Xmin = 0
	Xmax = 350
	Ymin = 0
	Ymax = 350
	pointClip(XY, 6, Xmin, Ymin, Xmax, Ymax)


