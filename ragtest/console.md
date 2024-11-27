```bash
(base) apple@appledeMacBook-Pro-2 KG-RAG % conda activate llm
(llm) apple@appledeMacBook-Pro-2 KG-RAG % mkdir -p ./ragtest/input
(llm) apple@appledeMacBook-Pro-2 KG-RAG % curl https://www.gutenberg.org/cache/epub/24022/pg24022.txt -o ./ragtest/input/book.txt
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  184k  100  184k    0     0   110k      0  0:00:01  0:00:01 --:--:--  110k
(llm) apple@appledeMacBook-Pro-2 KG-RAG % graphrag init --root ./ragtest
Initializing project at /Users/apple/Documents/project/KG-RAG/ragtest
⠋ GraphRAG Indexer %                                                                                   
(llm) apple@appledeMacBook-Pro-2 KG-RAG % graphrag index --root ./ragtest

Logging enabled at /Users/apple/Documents/project/KG-RAG/ragtest/logs/indexing-engine.log
🚀 create_base_text_units
Empty DataFrame
Columns: []
Index: []
🚀 create_final_documents
                                 id  ...                                      text_unit_ids
0  c305886e4aa2f6efcf64b57762777055  ...  [d6583840046247f428a9f02738842a7c, 10730234d6c...

[1 rows x 5 columns]
🚀 create_base_entity_graph
Empty DataFrame
Columns: []
Index: []
🚀 create_final_entities
                                  id  ...                                      text_unit_ids
0   d89b5fc86d3e430bba7f9054e293ea36  ...  [04e5c071e4ee5496d5380662e1339f45, 0f9b4e5a7cf...
1   c90012301d2448dca889ed3610c470de  ...                 
2   4b43c2ae5aed4bfda287e4ed59ef2ee6  ...                 
3   de8548515c8246c38d2112a0c9dac334  ...                 
4   ea3716d211934bad911dc4c56808e090  ...  [3763b08136628f77304cb4eb1136ea48, 4cf4deeb7f6...
5   fee2733f70824bfe850ba0e44d8f65ab  ...  [0f9b4e5a7cfc0c3c89a8898a45383588, 3763b081366...
6   4e48f1d352ac487a995be4bf355c78c0  ...                 [3763b08136628f77304cb4eb1136ea48]
7   bd73c6d46bb24bab9e87e8deb0b3144f  ...                 [3763b08136628f77304cb4eb1136ea48]
8   6a9e527abbc54f7a9790522b58d178e2  ...                 [3763b08136628f77304cb4eb1136ea48]
9   683e1463b52e448fa38272a2fa83357e  ...                 [3763b08136628f77304cb4eb1136ea48]
10  06d21ef7fe214fdca59a8002e3d7fb3d  ...  [4cf4deeb7f61acb7b7db4ce0e57fb1e6, 999c9887098...
11  e4a2a7bbe4ca4668a114dac327729b18  ...                 
12  112b2ac6a5774704b76285b204a75304  ...                 
13  eb7448e7f6434c91800c3402c50066e7  ...                 
14  a3eacc87124c4d129b659098693a71ec  ...  [4cf4deeb7f61acb7b7db4ce0e57fb1e6, ce95e4fc6ee...
15  d9cf21817fb94b2ca79e8a4d121d1df1  ...                 
16  c9aee5d4697f498abf22c3fb6fd40fbc  ...                 [999c9887098d1a25dc3b42a8da7ddc8c]
17  eac764dc4ce54dc69abb27092105d17e  ...                 [999c9887098d1a25dc3b42a8da7ddc8c]
18  ed996083de9e4f2c9fe7155a34755d17  ...                 [999c9887098d1a25dc3b42a8da7ddc8c]
19  3e28ec4ba0564b55b70b8ce8f105bce8  ...                 [999c9887098d1a25dc3b42a8da7ddc8c]
20  7a6b2ec5ee014af683b68f1f83ec2e87  ...                 [999c9887098d1a25dc3b42a8da7ddc8c]
21  140e886e99f545e991b637906bf2f6fb  ...                 [999c9887098d1a25dc3b42a8da7ddc8c]
22  a273699961d84d53a4b31730fd7cb9c7  ...                 [999c9887098d1a25dc3b42a8da7ddc8c]
23  f2fa31718b4843ec89f614c7a3c6be5d  ...                 [999c9887098d1a25dc3b42a8da7ddc8c]
24  3e2714391db64da4829755c2c7693838  ...                 [999c9887098d1a25dc3b42a8da7ddc8c]
25  9d35dd3a29b7414982f8987794b9da26  ...                 [999c9887098d1a25dc3b42a8da7ddc8c]
26  ce903c98d318494ca4637e52d9b73cbb  ...                 [999c9887098d1a25dc3b42a8da7ddc8c]
27  c7684d7f043c4811a7eb06899fdf03b3  ...  [04e5c071e4ee5496d5380662e1339f45, 4cf4deeb7f6...
28  1acc2693b15c4003ba20b78c3b1ab16b  ...  [04e5c071e4ee5496d5380662e1339f45, 4cf4deeb7f6...
29  628edde8c64a46c0b172c6a06541069d  ...                 [4cf4deeb7f61acb7b7db4ce0e57fb1e6]
30  2674c26a401e4927908039006c314d6f  ...  [0f9b4e5a7cfc0c3c89a8898a45383588, 4cf4deeb7f6...
31  aff18b41a2f24a60a7464b7fac59fe6f  ...                 [1cb66ea16e5e4f2816f0e188d3acc792]
32  ceed350922804da68d201d9d41a852b0  ...                 [1cb66ea16e5e4f2816f0e188d3acc792]
33  4aff026edf7e4be399e9f61ee707e4cc  ...                 [1cb66ea16e5e4f2816f0e188d3acc792]
34  2931c91f603247c0811e404ae2240cba  ...                 [1cb66ea16e5e4f2816f0e188d3acc792]
35  6c79751af3c94f7f84a2edf2be5c7c74  ...                 [1cb66ea16e5e4f2816f0e188d3acc792]
36  f2b2cc31369644cdaf039b900d15bcf4  ...                 [19f8fd68a8dbc1bba7058e13ce3a2e3d]
37  9bc841fbc6e54ac8931093dd6a56b072  ...  [19f8fd68a8dbc1bba7058e13ce3a2e3d, 6c362d3f8d0...
38  446092b53c16437082d820ec544326a1  ...                 [19f8fd68a8dbc1bba7058e13ce3a2e3d]
39  0978087147e744b09a678432ea8f73d6  ...                 [19f8fd68a8dbc1bba7058e13ce3a2e3d]
40  6820235f09854a72a00577825fc0357d  ...                 [19f8fd68a8dbc1bba7058e13ce3a2e3d]
41  5fc6586e611a4c81a2916c5058c356cd  ...                 [19f8fd68a8dbc1bba7058e13ce3a2e3d]
42  576e961ea48042c090b91af8f13d08b4  ...                 [0f9b4e5a7cfc0c3c89a8898a45383588]
43  c57c93e436d34cb3bd4e74a530650708  ...                 [0f9b4e5a7cfc0c3c89a8898a45383588]
44  6f5c7878bd34427cab6dbaf6c85992ee  ...  [0f9b4e5a7cfc0c3c89a8898a45383588, 6c362d3f8d0...
45  a50eefec2c434070960671c1a0270fc0  ...  [04e5c071e4ee5496d5380662e1339f45, 6c362d3f8d0...
46  d158a318f2ea480c92ccd49eafc487ca  ...                 [6c362d3f8d01c76d84443dcabf3f322a]
47  dd38ae95aa684541b990cec99fc3a2fc  ...                 [6c362d3f8d01c76d84443dcabf3f322a]
48  00399deb015d4753959c07e028ef3617  ...                 [6c362d3f8d01c76d84443dcabf3f322a]
49  57b489b03e4147008354b1464360a48e  ...                 [6c362d3f8d01c76d84443dcabf3f322a]
50  746784ac64194bec807decee82505896  ...                 [04e5c071e4ee5496d5380662e1339f45]
51  79572a09df5e473792398050ffb99aec  ...                 [04e5c071e4ee5496d5380662e1339f45]
52  c4d805779223421391092c31a18757be  ...                 
53  c9f6c446d9b748de908430998a60de34  ...                 
54  cb69c8e129e641be8a9bd1fac89e2e94  ...                 
55  d138b9947df84306b0e4f89d34343e28  ...                 
56  1feaf53a8bef4fb285504b862e73ffdc  ...                 
57  0441478d27574283aeac42a11ca5c9c2  ...                 
58  8c832564aa51492ab0e8b6b838ada871  ...                 

[59 rows x 6 columns]
🚀 create_final_nodes
                                  id  human_readable_id  ...  x  y
0   d89b5fc86d3e430bba7f9054e293ea36                  0  ...  0  0
1   c90012301d2448dca889ed3610c470de                  1  ...  0  0
2   4b43c2ae5aed4bfda287e4ed59ef2ee6                  2  ...  0  0
3   de8548515c8246c38d2112a0c9dac334                  3  ...  0  0
4   ea3716d211934bad911dc4c56808e090                  4  ...  0  0
5   fee2733f70824bfe850ba0e44d8f65ab                  5  ...  0  0
6   4e48f1d352ac487a995be4bf355c78c0                  6  ...  0  0
7   bd73c6d46bb24bab9e87e8deb0b3144f                  7  ...  0  0
8   6a9e527abbc54f7a9790522b58d178e2                  8  ...  0  0
9   683e1463b52e448fa38272a2fa83357e                  9  ...  0  0
10  06d21ef7fe214fdca59a8002e3d7fb3d                 10  ...  0  0
11  e4a2a7bbe4ca4668a114dac327729b18                 11  ...  0  0
12  112b2ac6a5774704b76285b204a75304                 12  ...  0  0
13  eb7448e7f6434c91800c3402c50066e7                 13  ...  0  0
14  a3eacc87124c4d129b659098693a71ec                 14  ...  0  0
15  d9cf21817fb94b2ca79e8a4d121d1df1                 15  ...  0  0
16  c9aee5d4697f498abf22c3fb6fd40fbc                 16  ...  0  0
17  eac764dc4ce54dc69abb27092105d17e                 17  ...  0  0
18  ed996083de9e4f2c9fe7155a34755d17                 18  ...  0  0
19  3e28ec4ba0564b55b70b8ce8f105bce8                 19  ...  0  0
20  7a6b2ec5ee014af683b68f1f83ec2e87                 20  ...  0  0
21  140e886e99f545e991b637906bf2f6fb                 21  ...  0  0
22  a273699961d84d53a4b31730fd7cb9c7                 22  ...  0  0
23  f2fa31718b4843ec89f614c7a3c6be5d                 23  ...  0  0
24  3e2714391db64da4829755c2c7693838                 24  ...  0  0
25  9d35dd3a29b7414982f8987794b9da26                 25  ...  0  0
26  ce903c98d318494ca4637e52d9b73cbb                 26  ...  0  0
27  c7684d7f043c4811a7eb06899fdf03b3                 27  ...  0  0
28  1acc2693b15c4003ba20b78c3b1ab16b                 28  ...  0  0
29  628edde8c64a46c0b172c6a06541069d                 29  ...  0  0
30  2674c26a401e4927908039006c314d6f                 30  ...  0  0
31  aff18b41a2f24a60a7464b7fac59fe6f                 31  ...  0  0
32  ceed350922804da68d201d9d41a852b0                 32  ...  0  0
33  4aff026edf7e4be399e9f61ee707e4cc                 33  ...  0  0
34  2931c91f603247c0811e404ae2240cba                 34  ...  0  0
35  6c79751af3c94f7f84a2edf2be5c7c74                 35  ...  0  0
36  f2b2cc31369644cdaf039b900d15bcf4                 36  ...  0  0
37  9bc841fbc6e54ac8931093dd6a56b072                 37  ...  0  0
38  446092b53c16437082d820ec544326a1                 38  ...  0  0
39  0978087147e744b09a678432ea8f73d6                 39  ...  0  0
40  6820235f09854a72a00577825fc0357d                 40  ...  0  0
41  5fc6586e611a4c81a2916c5058c356cd                 41  ...  0  0
42  576e961ea48042c090b91af8f13d08b4                 42  ...  0  0
43  c57c93e436d34cb3bd4e74a530650708                 43  ...  0  0
44  6f5c7878bd34427cab6dbaf6c85992ee                 44  ...  0  0
45  a50eefec2c434070960671c1a0270fc0                 45  ...  0  0
46  d158a318f2ea480c92ccd49eafc487ca                 46  ...  0  0
47  dd38ae95aa684541b990cec99fc3a2fc                 47  ...  0  0
48  00399deb015d4753959c07e028ef3617                 48  ...  0  0
49  57b489b03e4147008354b1464360a48e                 49  ...  0  0
50  746784ac64194bec807decee82505896                 50  ...  0  0
51  79572a09df5e473792398050ffb99aec                 51  ...  0  0
52  c4d805779223421391092c31a18757be                 52  ...  0  0
53  c9f6c446d9b748de908430998a60de34                 53  ...  0  0
54  cb69c8e129e641be8a9bd1fac89e2e94                 54  ...  0  0
55  d138b9947df84306b0e4f89d34343e28                 55  ...  0  0
56  1feaf53a8bef4fb285504b862e73ffdc                 56  ...  0  0
57  0441478d27574283aeac42a11ca5c9c2                 57  ...  0  0
58  8c832564aa51492ab0e8b6b838ada871                 58  ...  0  0

[59 rows x 8 columns]
🚀 create_final_communities
                                     id  human_readable_id  ...      period  size
0  947aec9b-9d23-4f20-8c02-e7eedf010242                  1  ...  2024-11-27    19
1  bd8280c0-b04c-4f29-8ae8-b0870b697d53                  6  ...  2024-11-27     2
2  f23bf469-4bea-4db8-b917-d25b3a7d73aa                  2  ...  2024-11-27     2
3  30e23cc4-8c7e-40d5-bfe2-20a85e02d649                  5  ...  2024-11-27     7
4  0284fd15-00fb-4964-8cf1-175db2c1f928                  3  ...  2024-11-27     3
5  36659091-c862-49bf-959e-72524d57ce37                  8  ...  2024-11-27     3
6  d68b540e-5025-49ac-a2e9-c5c7c6badb80                  4  ...  2024-11-27     4
7  8712fe7c-4e58-4f2e-8ed6-60a235b308aa                  7  ...  2024-11-27     4
8  85de6497-cd3c-4e29-b5d0-49852b0fbb9c                  0  ...  2024-11-27     4

[9 rows x 10 columns]
🚀 create_final_relationships
                                  id  ...                                      text_unit_ids
0   b1f54fda6e33400aaf481710f8637a63  ...                 
1   8eb7423d8d1347f0ba58349358043331  ...  [3763b08136628f77304cb4eb1136ea48, 4cf4deeb7f6...
2   078278252ed348dc85387bf1477dcc18  ...  [0f9b4e5a7cfc0c3c89a8898a45383588, 3763b081366...
3   4fcd275a5f6d4bf79a9e6ce441777d61  ...                 [3763b08136628f77304cb4eb1136ea48]
4   b1b057e74cb646a7a44ce86b8afd631e  ...                 [3763b08136628f77304cb4eb1136ea48]
..                               ...  ...                                                ...
56  ffcc7bdb56004defb2fd97ea557b5e77  ...                 
57  d624c669d7d54c7881eb9a00cdbec457  ...                 
58  978b72796bb44eed8e902732e12aacef  ...                 
59  f2467b55cdf644d59bc4869fda95102d  ...                 
60  38d1abd649244d1595471e7069e9372b  ...                 

[61 rows x 8 columns]
🚀 create_final_text_units
                                  id  ...                                   relationship_ids
0   d6583840046247f428a9f02738842a7c  ...                                               None
1   10730234d6ccc7cee08f3cfc58d8a9a1  ...                                               None
2   980594a50d68db06e6ca257bdb9ae95e  ...                                               None
3   080d8e696ff38c653ca90fa086415e74  ...                                               None
4   0e2b719e4c97d0d8bfeb2a53f7638eb6  ...                                               None
5   7064df4af064aeb556e5bab52e896414  ...                                               None
6   759315fa84c14e81f84fc71c73746184  ...                                               None
7   e8d4072836ac08145edc2fa8c15ea2c2  ...  [b1f54fda6e33400aaf481710f8637a63, f96a2ca0f17...
8   e3bef9514042131cf477476725497416  ...                                               None
9   4ffd9df98742c035b3e15bb24c3edb12  ...                                               None
10  8435b078474636a989a8c22f5493e1b6  ...                                               None
11  3763b08136628f77304cb4eb1136ea48  ...  [8eb7423d8d1347f0ba58349358043331, 078278252ed...
12  206c2f9fd249659c7a897d323459cb6f  ...                                               None
13  ce95e4fc6ee410973c040fc628dce155  ...  [ab3907c6d34f4f92aeef74dad0bacb55, d9b6e5f6bd2...
14  260fb94666cbdfb08286ce8d8162130d  ...                                               None
15  bf29edcb41403e5af43aa101072f4fdf  ...                                               None
16  d453d198afec5b284ff36024780b088c  ...                                               None
17  c79e67fc6f74a9afbe79c158000cc71b  ...                                               None
18  77ae3762a0b062ca5350ea54a05450ae  ...                                               None
19  b029f1164f623c14a0cfaa73c246f50d  ...                                               None
20  29793cee69d4eefd5fea8a5f2f27b521  ...                                               None
21  b4dec8fbe9f2a2c6a79d09c9484d15ae  ...                                               None
22  5d70b47bf7167b7586f47fcc4355a746  ...                                               None
23  1bdf253855a115bcf51faa63d7b07e82  ...                                               None
24  999c9887098d1a25dc3b42a8da7ddc8c  ...  [3e5e1eae8a6641ebbe12e2235de5bd4d, daf6c5744cc...
25  bc5fde5d1e00a3ecc1e548c8d24f1c1f  ...                                               None
26  4cf4deeb7f61acb7b7db4ce0e57fb1e6  ...  [8eb7423d8d1347f0ba58349358043331, ad257b7f50f...
27  61a042016835080f3d334560b13b0e35  ...                                               None
28  98f3970b31dfa1d7391cdaa453d6ade7  ...                                               None
29  ebc403dd3df39bacc3443ef4afb7edfd  ...                                               None
30  1cb66ea16e5e4f2816f0e188d3acc792  ...  [d79af6aea2f74ec4b798ee51e77031c9, f5320a481a3...
31  bc606176c752984da6d202275ee8c7a6  ...                                               None
32  cd8a47ace09b9cee1e8b27b0689f2822  ...                                               None
33  f40e4b274b5e1a25afbff9ecb733e1f4  ...                                               None
34  19f8fd68a8dbc1bba7058e13ce3a2e3d  ...  [02d203eab286444a9cab2bf0d2474bb4, a9a75574bf2...
35  0f9b4e5a7cfc0c3c89a8898a45383588  ...  [078278252ed348dc85387bf1477dcc18, 65691bb4bd6...
36  6c362d3f8d01c76d84443dcabf3f322a  ...  [02d203eab286444a9cab2bf0d2474bb4, 79a77ae3001...
37  04e5c071e4ee5496d5380662e1339f45  ...  [99683561da514edd8fa59f6ae1f68040, 2f2aab85320...
38  2b5ecb7fba1301d1f3d307e194a6c435  ...                                               None
39  aa8d2310a206001404282ddb3fd645aa  ...                                               None
40  0ddc17ea5e566006c000b4013f2181a5  ...                                               None
41  cd4234ed6caba8f15d09a2e3ee604b2a  ...  [2f1c0b0a465142ee8886728102f36628, ffcc7bdb560...

[42 rows x 7 columns]
🚀 create_final_community_reports
                                     id  human_readable_id  ...      period  size
0  a794d24b-1c16-4639-87f8-4bcce2560b40                 -1  ...         NaN   NaN
1  02a27beb-f63b-47a1-8574-04788e0258cd                  0  ...  2024-11-27   4.0
2  f6de5e90-a056-40e4-8fb2-45707ae81193                  1  ...  2024-11-27  19.0
3  5ea4fa01-7cae-4f8c-93f3-dacfba830007                  2  ...  2024-11-27   2.0
4  dedf3d7f-529d-44b4-98f9-b0f54de428ca                  3  ...  2024-11-27   3.0
5  03489fc6-2f30-4ffc-bbc2-b054220f3f20                  4  ...  2024-11-27   4.0
6  e3dc5b46-c951-41f5-a942-e426f89df46c                  5  ...  2024-11-27   7.0
7  60f7b0dc-2d8d-4cb0-8f5f-3b0cb73d80c5                  6  ...  2024-11-27   2.0
8  e2202f38-32d4-4bcd-94b5-7adbe32059ae                  7  ...  2024-11-27   4.0
9  43bece7d-40b8-4a89-95f1-be14f3255ef1                  8  ...  2024-11-27   3.0

[10 rows x 13 columns]
⠸ GraphRAG Indexer 
├── Loading Input (text) - 1 files loaded (0 filtered) ━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00 0:00:00
├── create_base_text_units
⠙ GraphRAG Indexer 
├── Loading Input (text) - 1 files loaded (0 filtered) ━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00 0:00:00
⠹ GraphRAG Indexer 
├── Loading Input (text) - 1 files loaded (0 filtered) ━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00 0:00:00
├── create_base_text_units
🚀 generate_text_embeddings
Empty DataFrame
Columns: []
Index: []
⠹ GraphRAG Indexer 
├── Loading Input (text) - 1 files loaded (0 filtered) ━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00 0:00:00
├── create_base_text_units
├── create_final_documents
├── create_base_entity_graph
├── create_final_entities
├── create_final_nodes
├── create_final_communities
├── create_final_relationships
├── create_final_text_units
├── create_final_community_reports
└── generate_text_embeddings
🚀 All workflows completed successfully.
(llm) apple@appledeMacBook-Pro-2 KG-RAG % 
```