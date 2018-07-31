.. _download-verify-uncompress-mac:

Download, verify, and uncompress a Clear Linux image on macOS\*
###############################################################

This guide describes the types of |CLOSIA| images available, where to download
them, how to verify the integrity of an image, and how to uncompress it.

Instructions for other operating systems are available:

* :ref:`download-verify-uncompress-linux`
* :ref:`download-verify-uncompress-windows`

Image types
***********

.. include:: ../../reference/image-types.rst
   :start-after: image-types-content:

.. _verify-mac:

Verify the integrity of the Clear Linux image
*********************************************

Before you use a downloaded |CL| image, verify its integrity. This action
eliminates the small chance of a corrupted image due to download issues. To
support verification, each released |CL| image has a corresponding SHA512
checksum file designated with the suffix `-SHA512SUMS`.

#. Download the corresponding SHA512 checksum file of your |CL| image.
#. Start the Terminal app.
#. Go to the directory with the downloaded image and checksum files.
#. Verify the integrity of the image and compare it to its original checksum
   with the command:

   .. code-block:: bash

	  shasum -a512 ./clear-[version number]-[image type].[compression type] | diff ./clear-[version number]-[image type].[compression type]-SHA512SUMS -

If the checksum of the downloaded image is different than the original
checksum, the differences will be displayed. Otherwise, an empty output indicates
a match and your downloaded image is good.

Uncompress the Clear Linux image
********************************

We compress all released |CL| images by default with either GNU zip 
(`.gz`) or xz (`.xz`). The compression type we use depends on the target 
platform or environment. To uncompress the image, follow these steps:

#. Start the Terminal app.
#. Go to the directory with the downloaded image.
#. Use the :command:`gunzip` command to uncompress either compression type. For example:

   .. code-block:: bash

	  gunzip clear-[version number]-[image type].xz
	  gunzip clear-[version number]-[image type].gz
