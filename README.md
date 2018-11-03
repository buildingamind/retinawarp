# Retina
Tensorflow implementation of fisheye transformation, mimicking the spatial sampling properties of the primate retina

# Dependencies
1. numpy

2. scipy

3. scikit-image

4. tensorflow

# How to install 
1. `cd [retina_directory_containing_setup.py]`
   
2. `pip install .` 

# How to use
For numpy implementation: 
    
    # Import functions
    from retina.retina import retina_warp
    
    # read your image
    img = imageio.imread('...')
    # transform
    warp_image(img, output_size=299)
    
For tensorflow implementation: 
    
    # Import functions
    from retina.retina_tf import warp_image
    
    # transform
    with tf.Session() as sess:
        img = imageio.imread('...')
        retina_img = warp_image(img, output_size=299)
        retina_img = retina_img.eval()

Look [here](notebooks/RetinaWarp.ipynb) for more details.