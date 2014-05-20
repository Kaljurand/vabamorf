
ex_etana = json/etana/
ex_etsyn = json/etsyn/
dct = ../dct/

all: help

help:
	@echo Targets:
	@echo
	@echo "  update_output_examples: overwrites the output examples based on the current etana/etsyn cmdline clients"

update_output_examples:
	etana analyze -lex $(dct) < $(ex_etana)ex1.json > $(ex_etana)ex1_analyze.json
	etana analyze -lex $(dct) -phonetic < $(ex_etana)ex1.json > $(ex_etana)ex1_analyze_phonetic.json
	etana analyze -lex $(dct) -phonetic < $(ex_etana)ex2.json > $(ex_etana)ex2_analyze_phonetic.json
	etana analyze -lex $(dct) -phonetic < $(ex_etana)test.json > $(ex_etana)test_analyze_phonetic.json
	etana analyze -lex $(dct) -guess -phonetic < $(ex_etana)test.json > $(ex_etana)test_analyze_guess_phonetic.json
	etsyn -lex $(dct) < $(ex_etsyn)ex2.json > $(ex_etsyn)ex2_syn.json
	etsyn -lex $(dct) < $(ex_etsyn)test.json > $(ex_etsyn)test_syn.json

test_json:
	find . -name "*.json" | while read json; do echo "$$json"; python -mjson.tool $$json > /dev/null; done
