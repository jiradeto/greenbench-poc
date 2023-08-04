# Micro-fuzzbench experiments

This document provides instructions for running the micro-fuzzbench experiments.

## Setup custom seeds

This branch contains a custom seed archive (custom_seeds.tar.gz) required to run experiments 3 to 6. To extract the custom seeds, you can run the following command from the project root directory:
```
tar xvf custom_seeds.tar.gz
```

## Running experiments

Please use the following commands to start each of the 6 experiments.

1. experiment 1-region-24h-20t
```bash
PYTHONPATH=. python3 experiment/run_experiment.py \
--experiment-config private-experiment-request/1-region-24h-20t/experiment-config.yaml \
--experiment-name 1-region-24h-20t \
--region-coverage \
--benchmarks bloaty_fuzz_target curl_curl_fuzzer_http freetype2-2017 harfbuzz-1.3.2 jsoncpp_jsoncpp_fuzzer lcms-2017-03-21 libjpeg-turbo-07-2017 libpcap_fuzz_both libpng-1.2.56 libxml2-v2.9.2 libxslt_xpath mbedtls_fuzz_dtlsclient openssl_x509 openthread-2019-12-23 php_php-fuzz-parser proj4-2017-08-14 re2-2014-12-09 sqlite3_ossfuzz systemd_fuzz-link-parser vorbis-2017-12-11 woff2-2016-05-06 zlib_zlib_uncompress_fuzzer
```

2. experiment 2-branch-24h-20t
```bash
PYTHONPATH=. python3 experiment/run_experiment.py \
--experiment-config private-experiment-request/2-branch-24h-20t/experiment-config.yaml \
--experiment-name 2-branch-24h-20t \
--benchmarks bloaty_fuzz_target curl_curl_fuzzer_http freetype2-2017 harfbuzz-1.3.2 jsoncpp_jsoncpp_fuzzer lcms-2017-03-21 libjpeg-turbo-07-2017 libpcap_fuzz_both libpng-1.2.56 libxml2-v2.9.2 libxslt_xpath mbedtls_fuzz_dtlsclient openssl_x509 openthread-2019-12-23 php_php-fuzz-parser proj4-2017-08-14 re2-2014-12-09 sqlite3_ossfuzz systemd_fuzz-link-parser vorbis-2017-12-11 woff2-2016-05-06 zlib_zlib_uncompress_fuzzer
```

3. experiment 3-branch-24h-20t-rd
```bash
PYTHONPATH=. python3 experiment/run_experiment.py \
--experiment-config private-experiment-request/3-branch-24h-20t-rd/experiment-config.yaml \
--experiment-name 3-branch-24h-20t-rd \
--custom-seed-corpus-dir custom_seeds \
--benchmarks bloaty_fuzz_target curl_curl_fuzzer_http freetype2-2017 harfbuzz-1.3.2 jsoncpp_jsoncpp_fuzzer lcms-2017-03-21 libjpeg-turbo-07-2017 libpcap_fuzz_both libpng-1.2.56 libxml2-v2.9.2 libxslt_xpath mbedtls_fuzz_dtlsclient openssl_x509 openthread-2019-12-23 php_php-fuzz-parser proj4-2017-08-14 re2-2014-12-09 sqlite3_ossfuzz systemd_fuzz-link-parser vorbis-2017-12-11 woff2-2016-05-06 zlib_zlib_uncompress_fuzzer
```

4. experiment 4-branch-15m-20t-rd
```bash
PYTHONPATH=. python3 experiment/run_experiment.py \
--experiment-config private-experiment-request/4-branch-15m-20t-rd/experiment-config.yaml \
--experiment-name 4-branch-15m-20t-rd \
--custom-seed-corpus-dir custom_seeds \
--benchmarks bloaty_fuzz_target curl_curl_fuzzer_http freetype2-2017 harfbuzz-1.3.2 jsoncpp_jsoncpp_fuzzer lcms-2017-03-21 libjpeg-turbo-07-2017 libpcap_fuzz_both libpng-1.2.56 libxml2-v2.9.2 libxslt_xpath mbedtls_fuzz_dtlsclient openssl_x509 openthread-2019-12-23 php_php-fuzz-parser proj4-2017-08-14 re2-2014-12-09 sqlite3_ossfuzz systemd_fuzz-link-parser vorbis-2017-12-11 woff2-2016-05-06 zlib_zlib_uncompress_fuzzer
```

5. experiment 5-branch-15m-100t-rd
```bash
PYTHONPATH=. python3 experiment/run_experiment.py \
--experiment-config private-experiment-request/5-branch-15m-100t-rd/experiment-config.yaml \
--experiment-name 5-branch-15m-100t-rd \
--custom-seed-corpus-dir custom_seeds \
--benchmarks bloaty_fuzz_target curl_curl_fuzzer_http freetype2-2017 harfbuzz-1.3.2 jsoncpp_jsoncpp_fuzzer lcms-2017-03-21 libjpeg-turbo-07-2017 libpcap_fuzz_both libpng-1.2.56 libxml2-v2.9.2 libxslt_xpath mbedtls_fuzz_dtlsclient openssl_x509 openthread-2019-12-23 php_php-fuzz-parser proj4-2017-08-14 re2-2014-12-09 sqlite3_ossfuzz systemd_fuzz-link-parser vorbis-2017-12-11 woff2-2016-05-06 zlib_zlib_uncompress_fuzzer
```

6. experiment 6-branch-15m-100t-rd-target
```bash
PYTHONPATH=. python3 experiment/run_experiment.py \
--experiment-config private-experiment-request/6-branch-15m-100t-rd-target/experiment-config.yaml \
--experiment-name 6-branch-15m-100t-rd-target \
--custom-seed-corpus-dir custom_seeds \
--benchmarks bloaty_fuzz_target curl_curl_fuzzer_http freetype2-2017 harfbuzz-1.3.2 jsoncpp_jsoncpp_fuzzer lcms-2017-03-21 libjpeg-turbo-07-2017 libpcap_fuzz_both libpng-1.2.56 libxml2-v2.9.2 libxslt_xpath mbedtls_fuzz_dtlsclient openssl_x509 openthread-2019-12-23 php_php-fuzz-parser proj4-2017-08-14 re2-2014-12-09 sqlite3_ossfuzz systemd_fuzz-link-parser vorbis-2017-12-11 woff2-2016-05-06 zlib_zlib_uncompress_fuzzer
```
