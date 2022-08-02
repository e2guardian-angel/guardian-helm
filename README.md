# guardian-helm
Helm charts for the e2guardian-angel stack

## e2guardian config
### Phrase list format
```
name: 'myphraselist'
includeIn: 
- 'bannedsitelist'
groups:
- name: 'bad category 1'
  phrases:
  - '<word1>,<word2>'
- name: 'bad category 2'
  phrases:
  - '<word3>,<word4>'
```
### Weighted phrase list format
```
name: 'myweightedphraselist'
includeIn: 
- 'weightedphraselist'
groups:
- name: 'bad category 1'
  phrases:
  - phrase: '<word1>,<word2>'
    weight: 12
- name: 'good category 2'
  phrases:
  - phrase: '<word3>,<word4>'
    weight: -10
```
## other list format
This format works for site lists, mime type lists, extension lists, etc.
```
name: 'mysitelist'
includeIn:
- 'bannedsitelist'
groups:
- name: 'bad category 1
  items:
  - 'badsite1.com'
  - 'badsite2.com'
```
## example
```
lists:
  - name: 'mybannedextensions'
    includeIn:
    - 'bannedmimetypelist'
    groups:
    - items:
      - 'video/msvideo'
      - 'video/x-msvideo'
    - name: 'zip'
      items:
      - 'application/gzip'
      - 'application/x-gzip'
```