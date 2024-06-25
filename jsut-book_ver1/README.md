# PJS: Phoneme-balanced Japanese Singing-voice corpus
Japanese follows English. 

日本語の記述は英語に続きます．

## Description / 内容
This corpus consists of audiobook voice data. The specification is as follows.
 - Speaker: a female non-professional Japanese speaker. The speaker is the same to that of JSUT, JSUT-song, JSUT-vi corpora. 
- Size: 6 audiobooks, 1 hours of voice
- Recording: 48 kHz sampling, studio recording
- Data: text (\*.yaml), voice (\*.wav)．The text file contains chapter ('chaptXXX'), paragraph ('paragXXX'), style ('narration' or acting character's names), raw sentence, sentence-level alignment.

このコーパスはオーディオブック音声から成ります．日本語テキストと多数話者の音声データからなります．スペックは以下のとおりです．
- 話者： プロではない日本語女性話者1名．この話者は，JSUT, JSUT-song, JSUT-vi コーパスの話者と同じです．
- サイズ： 6つの物語，１時間の音声
- 収録：48kHz サンプリング，スタジオ収録
- データ： テキスト (\*.yaml)，音声 (\*.wav)．テキストファイルには，章 ('chapterXXX')，段落 ('paragraphXXX')，様式 ('narration' もしくは キャラ名)，文，文レベルのアライメント結果が含まれています．

## Tips / 役立つ情報
Some kanji in the raw sentence have their furigana (reading aid consisting of hiragana), e.g., `お[菓子|かし]がひとつ`. You can choose a favorite style as
```
# python
import re

x = "お[菓子|かし]がひとつ"           # [kanji|furigana]
re.sub('\[(\w+)\|(\w+)\]', r'$1', x)  # お菓子がひとつ
re.sub('\[(\w+)\|(\w+)\]', r'$2', x)  # おかしがひとつ
```

## Terms of use / 使い方
The text data is out-of-copyright books stored in the Aozora Bunko. The audio data may be used for 
- Research by academic institutions
- Non-commercial research, including research conducted within commercial organizations
- Personal use, including blog posts.

If you want to use for commercial purposes, please see below. Re-distribution is not permitted, but you can upload a part of this corpus (e.g., ~10 audio files) in your website or blog. If possible, please let me know when you revealed papers, blog posts, and others. It will be very helpful to investigate contributions of this corpus. 

テキストデータは青空文庫に収録されている，著作権切れの文です．音声データは，以下の場合に限り使用可能です．
- アカデミック機関での研究
- 非商用目的の研究（営利団体での研究も含む）
- 個人での利用（ブログなどを含む）

営利目的の利用を希望される場合，下記をご覧ください．この音声データの再配布は認められていませんが，あなたのウェブページやブログなどでコーパスの一部（例えば，10文程度）を公開することは可能です．できれば，あなたが論文やブログポスト等の成果を公開した際には，私まで連絡してもらえると助かります．このコーパスの貢献を調査することは，我々にとって非常に有効な情報となります．

## Contributors / 作成者
- Shinnosuke Takamichi (University of Tokyo) / 高道 慎之介 (東京大学)
- Hiroshi Saruwatari (University of Tokyo) / 猿渡 洋 (東京大学)

## Paper / 論文
No paper. Please cite our project page.

## Acknowledgement / 謝辞 
This research was supporeted by the GAP fund project of the University of Tokyo. 

本プロジェクトは，東京大学 GAPファンドの支援を受けて実施した．

## Link / リンク
- JSUT-book corpus project page: https://sites.google.com/site/shinnosuketakamichi/publication/jsut-book