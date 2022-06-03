# IMPORT LIBRARIES

import pygame
import sys
import random

pygame.init()
# Load source image
source_image = pygame.image.load(sys.argv[1])

#get the width and height of source image and use a scaling factor of 5 for the new image
(wid, hgt) = source_image.get_size()
w = (wid * 5)  
h = (hgt * 5)

#set the drawing window
drawing_window = pygame.display.set_mode((w, h))

#Set the file to save the new image
external_file = open("pointed_image.jpg", "w")

#Get the RGB values of each pixel of the source image
for pixel_hgt_pos in range(hgt):
	for pixel_wid_pos in range(wid):
		(r, g, b, _) = source_image.get_at((pixel_wid_pos, pixel_hgt_pos))
		
		#get the ratio of the RGB in the pixel
		red_ratio = r // 150
		green_ratio = g // 150
		blue_ratio = b // 150	
					
		#set the range of random values for the points to be placed on the new image
		
		
		#based on the ratio of the RGB values draw the correspondent number of points on the new image
						
		for r_value_counter in range(red_ratio):
			x_stop = int((pixel_wid_pos + 0.9) * 5)
			y_stop = int((pixel_hgt_pos + 0.9) * 5)
			new_x = random.randint((pixel_wid_pos * 5), (x_stop))
			new_y = random.randint((pixel_hgt_pos * 5), (y_stop))		
			pygame.draw.rect(drawing_window, (255, 0, 0), (new_x, new_y, 1, 1))
		for g_value_counter in range(green_ratio):
			x_stop = int((pixel_wid_pos + 0.9) * 5)
			y_stop = int((pixel_hgt_pos + 0.9) * 5)
			new_x = random.randint((pixel_wid_pos * 5), (x_stop))
			new_y = random.randint((pixel_hgt_pos * 5), (y_stop))	
			pygame.draw.rect(drawing_window, (0,255, 0), (new_x, new_y, 1, 1))
		for b_value_counter in range(blue_ratio):
			x_stop = int((pixel_wid_pos + 0.9) * 5)
			y_stop = int((pixel_hgt_pos + 0.9) * 5)
			new_x = random.randint((pixel_wid_pos * 5), (x_stop))
			new_y = random.randint((pixel_hgt_pos * 5), (y_stop))	
			pygame.draw.rect(drawing_window, (0, 0, 255), (new_x, new_y, 1, 1))				
				
#save the image on an external file							
	print(file=external_file)
			
			

external_file.close()
		
pygame.display.update()		
	
while True:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            exit()
