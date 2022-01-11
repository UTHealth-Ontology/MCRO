IMPORTS
===============

target file used was swo-merged.owl from https://github.com/allysonlister/swo/tree/master/dev/ontology

EXTRACT
--------------
`robot extract --method BOT --input swo-merged.owl --term-file swo-seed.txt --individuals exclude --intermediates all --copy-ontology-annotations true  --output swo_import_bot.owl` 

`robot extract --method TOP --input swo-merged.owl --term-file swo-seed.txt --individuals exclude --intermediates all --copy-ontology-annotations true  --output swo_import_top.owl`

`robot extract --method STAR --input swo-merged.owl --term-file swo-seed.txt --individuals exclude --intermediates all --copy-ontology-annotations true --output swo_import_star.owl`


MERGE
---------
`robot merge --input swo_import_bot.owl --input swo_import_top.owl --input swo_import_star.owl --output swo_import_intermediate.owl`


REMOVE
---------
`robot remove --input swo_import_intermediate.owl --term http://www.obofoundry.org/ro/ro.owl#has_part --term http://www.obofoundry.org/ro/ro.owl#part_of --select "self descendants" --signature true --output swo_import_pre1.owl`

`robot remove --input swo_import_pre1.owl --term http://www.ebi.ac.uk/swo/SWO_0000001 --select "descendants" --signature true --output swo_import_final.owl`