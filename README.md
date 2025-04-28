# documents 
from gimpfu import *

def cartoonify(img, layer):
    pdb.gimp_image_duplicate(img)
    pdb.plug_in_cartoon(img, layer, 10.0, 0.2)

register(
    "python_fu_cartoonify",
    "Cartoonify Image",
    "Applies a cartoon effect to an image",
    "Your Name", "Your Name", "2025",
    "<Image>/Filters/Artistic/Cartoonify...",
    "*",
    [],
    [],
    cartoonify)

main()
