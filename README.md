pdf_info
==

Very simple wrapper to the pdfinfo unix tool, to provide the metadata information as a hash.

Example
--

    require 'pdf/info'
    info = PDF::Info.new('/Users/tom/tmp/magazine.pdf')
    pp info.metadata

Gives you the following output:

    {:version=>1.3,
     :pages=>
      [[819.213, 1077.17],
       [819.213, 1077.17],
       [819.213, 1077.17],
       [819.213, 1077.17],
       [819.213, 1077.17],
       [819.213, 1077.17],
       [819.213, 1077.17],
       [819.213, 1077.17],
       [819.213, 1077.17],
       [819.213, 1077.17],
       [819.213, 1077.17],
       [819.213, 1077.17]],
     :page_count=>12,
     :encrypted=>false}
   
Each of the pages has an individual size - that's just how PDFs are. If you want more of the metadata that pdfinfo outputs, send us a patch.