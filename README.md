# secPublic
testing environment：
	Windows 10 20H2

results:\n
1.Out-Of-Bounds (OOB)
  fuzzPDFTron.exe id_000014_00_EXCEPTION_ACCESS_VIOLATION
  crash：OOBR[0x34]+4 b38.738 @ fuzzpdftron.exe!pdfnetc.dll+0xA60894.html
2.Access Violation write
