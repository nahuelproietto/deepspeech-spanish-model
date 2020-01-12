M-AILABS Spanish Corpus - es_ES - Español Ibérico
http://www.caito.de/data/Training/stt_tts/

108 hours and 34 minutes of annotated spanish.

The M-AILABS Speech Dataset is the first large dataset that we are providing free-of-charge.
Freely usable as training data for speech recognition and speech synthesis. 

Tensorflow pre-trained model for deepspeech.

DEEPSPEECH VERSION: 0.4.1
https://github.com/mozilla/DeepSpeech

154 samples failed upon conversion
7991 samples were longer than 10 seconds
imported 47686

High error % rate, recommended for testing or development.

Parameters used for training.

python3 ../DeepSpeech.py \
--train_files ./clips/train.csv \
--test_files ./clips/test.csv \
--dev_files ./clips/dev.csv \
--train_batch_size 80 \
--dev_batch_size 80 \
--test_batch_size 40 \
--n_hidden 2048 \
--epoch 1 \
--validation_step 1 \
--early_stop True \
--earlystop_nsteps 6 \
--estop_mean_thresh 0.1 \
--estop_std_thresh 0.1 \
--dropout_rate 0.22 \
--learning_rate 0.00095 \
--report_count 100 \
--use_seq_length False \
--export_dir "export" \
--checkpoint_dir "checkpoint" \
--decoder_library_path ./bin/libdeepspeech.so \
--alphabet_config_path ./alphabet.txt \
--lm_binary_path ./lm.binary \
--lm_trie_path ./trie
