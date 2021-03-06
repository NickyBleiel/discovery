---

copyright:
  years: 2015, 2017, 2019
lastupdated: "2019-01-28"

subcollection: discovery

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:pre: .pre}
{:important: .important}
{:deprecated: .deprecated}
{:codeblock: .codeblock}
{:screen: .screen}
{:download: .download}
{:hide-dashboard: .hide-dashboard}
{:apikey: data-credential-placeholder='apikey'} 
{:url: data-credential-placeholder='url'}
{:curl: #curl .ph data-hd-programlang='curl'}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:ruby: .ph data-hd-programlang='ruby'}
{:swift: .ph data-hd-programlang='swift'}
{:go: .ph data-hd-programlang='go'}

# 데이터 저장소 크롤링
{: #crawling-your-data-repository}

크롤러 옵션이 올바르게 구성된 후 데이터 저장소에 대해 크롤링을 실행할 수 있습니다.
{: shortdesc}

Data Crawler는 파일 공유 또는 데이터베이스를 크롤링하기 위해서만 사용되어야 합니다. 기타 모든 경우에는 적합한 {{site.data.keyword.discoveryshort}} 커넥터를 사용해야 합니다. 자세한 사항은 [데이터 소스에 연결](/docs/services/discovery?topic=discovery-sources#sources)을 참조하십시오. {{site.data.keyword.discoveryshort}} 커넥터에서 지원되는 데이터 소스를 사용하여 Data Crawler를 사용하는 경우 Data Crawler에 대한 지원이 더 이상 제공되지 않습니다.
{: important}

`root`만 읽을 수 있는 파일에 액세스해야 하는 경우 외에는, 크롤러를 `root`로 실행하지 마십시오.
{: tip}

`crawler` 명령을 실행하십시오.

크롤러는 수행할 작업에 대해 설명하는 문서와 함께 사용자에게 프롬프트를 표시합니다. 기타 크롤링 옵션을 추가하여 테스트 크롤링을 실행하거나 크롤링을 실행할 수 있습니다.

## 테스트 크롤링 실행
{: #running-test-crawl}

`crawler testit` 명령을 실행하십시오.

이를 통해 seed URL만 크롤링하고 큐에 삽입된 URL을 표시하는 테스트 크롤링이 실행됩니다. seed URL을 통해 인덱싱 가능한 컨텐츠(예: 문서)가 작성되는 경우 컨텐츠가 출력 어댑터에 전송되고 컨텐츠가 화면에 인쇄됩니다. seed URL 검색으로 인해 URL이 큐에 삽입되면 이러한 URL이 표시되고 컨텐츠가 출력 어댑터에 전송되지 않습니다. 기본적으로 큐에 삽입된 다섯 개의 URL이 표시됩니다.

크롤링 명령을 위한 옵션으로 사용자 정의 구성 파일을 지정할 수도 있습니다(예: `crawler testit --config [config/myconfigfile.conf]`).

`--config` 옵션에 전달된 구성 파일에 대한 경로는 완전한 경로여야 합니다. 즉, 상대 형식(예: `config/myconfigfile.conf` 또는 `./myconfigfile.conf`)으로 되어 있거나 절대 경로(예: `/path/to/config/myconfigfile.conf`)로 되어 있어야 합니다.

testit 명령을 위한 옵션으로 표시되는 큐에 삽입된 URL의 수에 대한 제한을 설정할 수도 있습니다(예: `crawler testit --limit [number]`).

## 크롤링 실행
{: #running-crawl}

`crawler crawl` 명령을 실행하십시오.

이를 통해 기본 구성 파일(`crawler.conf`)로 크롤링이 실행됩니다.

크롤링 명령을 위한 옵션으로 사용자 정의 구성 파일을 지정할 수도 있습니다(예: `crawler crawl --config [config/myconfigfile.conf]`).

`--config` 옵션에 전달된 구성 파일에 대한 경로는 완전한 경로여야 합니다. 즉, 상대 형식(예: `config/myconfigfile.conf` 또는 `./myconfigfile.conf`)으로 되어 있거나 절대 경로(예: `/path/to/config/myconfigfile.conf`)로 되어 있어야 합니다.

## 크롤링 재시작
{: #restarting-crawl}

`crawler restart` 명령을 실행하십시오.

이 명령을 통해 기본 구성 파일(`crawler.conf`)로 새 크롤링을 시작하여 크롤링이 재실행됩니다.

재시작 명령을 위한 옵션으로 사용자 정의 구성 파일을 지정할 수도 있습니다(예: `crawler restart --config [config/myconfigfile.conf]`).

`--config` 옵션에 전달된 구성 파일에 대한 경로는 완전한 경로여야 합니다. 즉, 상대 형식(예: `config/myconfigfile.conf` 또는 `./myconfigfile.conf`)으로 되어 있거나 절대 경로(예: `/path/to/config/myconfigfile.conf`)로 되어 있어야 합니다.

## 크롤링 재개
{: #resuming-crawl}

`crawler resume` 명령을 실행하십시오.

이 명령을 통해 기본 구성 파일(`crawler.conf`)로 크롤링이 중지된 위치에서 크롤링이 재개됩니다.

재개 명령을 위한 옵션으로 사용자 정의 구성 파일을 지정할 수도 있습니다(예: `crawler resume --config [config/myconfigfile.conf]`).

`--config` 옵션에 전달된 구성 파일에 대한 경로는 완전한 경로여야 합니다. 즉, 상대 형식(예: `config/myconfigfile.conf` 또는 `./myconfigfile.conf`)으로 되어 있거나 절대 경로(예: `/path/to/config/myconfigfile.conf`)로 되어 있어야 합니다.

## 크롤링 새로 고치기
{: #refresh-crawl}

`crawler refresh` 명령을 실행하십시오.

이 명령을 통해 기본 구성 파일(`crawler.conf`)로 이전 크롤링의 새로 고치기가 실행됩니다.

새로 고치기 명령을 위한 옵션으로 사용자 정의 구성 파일을 지정할 수도 있습니다(예: `crawler refresh --config [config/myconfigfile.conf]`).

`--config` 옵션에 전달된 구성 파일에 대한 경로는 완전한 경로여야 합니다. 즉, 상대 형식(예: `config/myconfigfile.conf` 또는 `./myconfigfile.conf`)으로 되어 있거나 절대 경로(예: `/path/to/config/myconfigfile.conf`)로 되어 있어야 합니다.
