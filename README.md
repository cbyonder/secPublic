# secPublic
1.testing environment:    
  Windows 10 20H2
  
2.get the pdfnet.dll  
downlaod PDFTron's C++ PDF library  for Windows(32-bit) from:  
https://www.pdftron.com/documentation/windows/get-started/cpp/    

3.prepare  
Put fuzzpdftron.exe, pdfnet.dll and input files in the same directory

4.run&&results  
1).Out-Of-Bounds (OOB)  
  fuzzPDFTron.exe id_000014_00_EXCEPTION_ACCESS_VIOLATION   
  crash: "OOBR[0x34]+4 b38.738 @ fuzzpdftron.exe!pdfnetc.dll+0xA60894.html"   
2).unallocated memory write  
  fuzzPDFTron.exe id_000048_00_EXCEPTION_ACCESS_VIOLATION  
  crash: "AVW.Reserved[0xC1000]@0xD6C 40e.722 @ fuzzpdftron.exe!pdfnetc.dll+0xA5F1F7.html"
