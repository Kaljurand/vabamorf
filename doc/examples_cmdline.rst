Commandline examples
====================

The input and output examples are available in the subdirectory `json`.

etana
-----

The input/output format of `etana` is based on JSON and documented
in <http://www.hm.ee/index.php?popup=download&id=11970>. With the
following differences:

  - 'word' is renamed to 'text'

Examples::

    etana analyze -lex ../dct/ < json/ex1.json > json/ex1_analyze.json

    etana analyze -lex ../dct/ -phonetic < json/ex1.json > json/ex1_analyze_phonetic.json


etsyn
-----

The input/output format of `etana` is based on JSON.

Examples::

    etsyn -lex ../dct/ < json/ex2.json > json/ex2_syn.json
