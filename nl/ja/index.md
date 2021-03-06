---

copyright:
  years: 2015, 2017
lastupdated: "2017-5-19"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Continuous Delivery 概説
{: #cd_getting_started}

アプリケーションのビルドとデプロイメントを自動化するオープン・ツールチェーンが組み込まれた {{site.data.keyword.contdelivery_full}} を使用することによって、DevOps アプローチを取り入れることができます。開発、デプロイメント、運用の作業をサポートする単純なデプロイメント・ツールチェーンを作成することから始めることができます。
{: shortdesc}

{{site.data.keyword.Bluemix_notm}} カタログから選択して {{site.data.keyword.contdelivery_short}} のインスタンスを作成した後、サービスにどのように取り掛かるかを選択できます。![Continuous Delivery ウェルカム・ページ](images/cd_landing_page.png)

* 自動化パイプラインを使用して迅速に始めてアプリケーションをデプロイするには、「パイプラインで開始 (Starting with a pipeline)」セクションで、**[「ここから開始 (Start here)](#starting_with_a_pipeline)**をクリックします。後でさらにツールを追加できます。
* テンプレートから継続的デリバリー・ツールチェーンを作成して構成するには、「ツールチェーン・テンプレートから開始 (Starting from a toolchain template)」セクションで、**[「ここから開始 (Start here)」](#starting_from_a_toolchain_template)**をクリックします。ツールチェーンは、パイプラインのプランニング、開発、デプロイと、アプリケーションの管理のためのツールを統合したものです。ツールチェーンに対していつでもツールを追加したり削除したりできます。
* ツールチェーンが既にある場合は、「ツールチェーン・テンプレートから開始 (Starting from a toolchain template)」セクションで、**「ツールチェーンを表示 (View your toolchains)」**をクリックします。ツールチェーンの扱いについて詳しくは、[ツールチェーンの使用](/docs/services/ContinuousDelivery/toolchains_using.html){: new_window}を参照してください。

**ヒント:** パイプラインはツールチェーンによって管理されます。パイプラインは既存のツールチェーンに追加できます。パイプラインを作成すると、既存のツールチェーンがなければ、デフォルト名のツールチェーンが自動で作成されます。ツールチェーンを使用して、他のツールやサービスと統合することで、パイプラインの機能を展開できます。

##{{site.data.keyword.contdelivery_short}} の概要
{: #cd_overview}

{{site.data.keyword.contdelivery_short}} は、DevOps プラクティスや業界最高レベルのツールを使用したアプリケーションのビルド、テスト、デリバリーを可能にします。
{:shortdesc}

{{site.data.keyword.contdelivery_short}} サービスは、以下の DevOps ワークフローをサポートします。

 * 統合された DevOps のオープン・[ツールチェーン](/docs/services/ContinuousDelivery/toolchains_about.html){: new_window}を作成して、開発、デプロイメント、および運用の各タスクをサポートするツール統合を可能にできます。

  ツールチェーンとは、アプリケーションを共同で開発、ビルド、デプロイ、テスト、管理するために使用できる統合ツール・セットです。ツールチェーンを使用すると、操作を反復可能にして管理しやすくすることができます。ツールチェーンには、オープン・ソース・ツール、{{site.data.keyword.Bluemix_notm}} サービス ([{{site.data.keyword.DRA_full}}](/docs/services/ContinuousDelivery/di_working.html){: new_window} など)、およびサード・パーティー製のツール (GitHub、PagerDuty、Slack など) を含めることができます。 

 * 自動化された[パイプライン](/docs/services/ContinuousDelivery/pipeline_about.html){: new_window}を使用すれば、継続的なデリバリーが可能になります。

  ビルド、単体テスト、デプロイメントなどを自動化します。最小限の人的介入で、反復可能な方法でビルド、テスト、デプロイします。いつでも実稼動環境で使用できるよう準備します。

 * [Web ベースの IDE](/docs/services/ContinuousDelivery/web_ide.html){: new_window} を使用して、どこからでもコードを編集してプッシュします。

  GitHub でソース管理のタスクの作成、編集、実行、デバッグ、完成を行えます。コードの編集から実稼動環境へのデプロイに、シームレスに移ります。 
  
 * IBM がホストする GitLab Community Edition ベースの [Git repository (repos) and issue tracker](/docs/services/ContinuousDelivery/git_working.html#git_working){: new_window} を使用して、チームのコラボレーションやソース・コードの管理を行えます。

  コードを保護するきめ細かいアクセス制御を通して Git リポジトリーを管理します。マージ要求を使用して、コードをレビューし、コラボレーションを向上させます。Issue Tracker を介して問題を追跡し、アイデアを共有します。Wiki システム上にプロジェクトを文書化します。

##パイプラインで開始 (Starting with a pipeline)
{: #starting_with_a_pipeline}

パイプラインは、ビルドやデプロイメントなどを自動化します。自動化パイプラインを開始するには、テンプレートを選択し、GitHub リポジトリーの場所を指定します。

Cloud Foundry アプリケーションをデプロイするように構成された[パイプラインを作成する ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.bluemix.net/devops/pipelines/dashboard/create){:new_window} には、以下のステップを実行します。

1. **「Cloud Foundry」**をクリックします。
1. パイプラインに別の名前を使用する場合は、デフォルトの名前を変更します。{{site.data.keyword.Bluemix_notm}} では、パイプラインはその名前で識別されます。
1. アプリケーションに別の名前を使用する場合は、デフォルトの名前を変更します。{{site.data.keyword.Bluemix_notm}} では、アプリケーションはその名前で識別されます。この名前は、パイプラインのデプロイ先のアプリケーションです。
1. ツールチェーンがない場合は、デフォルトの名前が付いたツールチェーンが作成されます。ツールチェーンに別の名前を使用する場合は、名前を変更します。パイプラインはツールチェーンによって管理されます。ツールチェーンを使用して、他のツールやサービスと統合することで、パイプラインの機能を拡張できます。

 **ヒント**: パイプラインとツールチェーンは、組織に属しています。ツールチェーンを持つ組織に属していれば、これらのツールチェーンの作成者でなくても使用することができます。

1. 使用するツールチェーンを選択するか、作成する新しいツールチェーンの名前を入力します。
1. Git プロバイダーを選択します。

 **ヒント**: ご使用の GitHub アカウントにアクセスする権限が {{site.data.keyword.Bluemix_notm}} にない場合は、**「許可 (Authorize)」**をクリックして GitHub Web サイトに移動するよう求められます。アクティブな GitHub セッションがない場合は、ログインするよう求められます。**「アプリケーションを許可 (Authorize Application)」** をクリックして、{{site.data.keyword.Bluemix_notm}} が GitHub アカウントにアクセスできるようにします。

 {{site.data.keyword.ghe_short}} リポジトリーへのアクセスを許可されていない場合は、リポジトリーの管理特権を持つユーザーに依頼して追加してもらう必要があります。{{site.data.keyword.Bluemix_notm}} Dedicated for {{site.data.keyword.ghe_short}} での許可の説明については、[{{site.data.keyword.Bluemix_notm}} Dedicated for {{site.data.keyword.ghe_short}} 概説](/docs/services/ghededicated/index.html){: new_window}を参照してください。ユーザー自身が管理する {{site.data.keyword.ghe_short}} のバージョンで許可する必要がある場合は、内部プロシージャーに従ってください。

    * 既存のリポジトリーを使用する場合は、リポジトリーのタイプとして**「リンク (Link)」**を選択します。リポジトリーの場所を検索するか、選択可能なリポジトリーのリストからリポジトリーを選択します。

    * 空のリポジトリーを作成する場合は、リポジトリー・タイプとして**「新規」**を選択します。リポジトリーの名前を入力します。

    * リポジトリーのクローンを作成する場合は、リポジトリーのタイプに**「コピー」**を選択します。リポジトリーの場所を検索するか、選択可能なリポジトリーのリストからリポジトリーを選択します。

    * リポジトリーをフォークし、プル・リクエストで変更内容を提供できるようにする場合は、**「フォーク (Fork)」**を選択します。リポジトリーの場所を検索するか、選択可能なリポジトリーのリストからリポジトリーを選択します。

1. リポジトリーを選択するか、リポジトリーの URL を入力します。
1. **「作成」**をクリックします。パイプラインが作成され、構成されて、ツールチェーンの「概要」ページに表示されます。![パイプライン・カード](images/cd_pipeline.png)

事前構成されたステージのない[空のパイプライン ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.bluemix.net/devops/pipelines/dashboard/create){: new_window} を作成するには、以下のようにします。

1. **「カスタム」**をクリックします。
1. パイプラインに別の名前を使用する場合は、デフォルトの名前を変更します。{{site.data.keyword.Bluemix_notm}} では、パイプラインはその名前で識別されます。
1. ツールチェーンがない場合は、デフォルトの名前が付いたツールチェーンが作成されます。ツールチェーンに別の名前を使用する場合は、名前を変更します。パイプラインはツールチェーンによって管理されます。ツールチェーンを使用して、他のツールやサービスと統合することで、パイプラインの機能を拡張できます。
1. 使用するツールチェーンを選択するか、作成する新しいツールチェーンの名前を入力します。
1. **「作成」**をクリックします。空のパイプラインが作成され、ツールチェーンの「概要」ページ上にカードとして表されます。

##ツールチェーン・テンプレートから開始 (Starting from a toolchain template)
{: #starting_from_a_toolchain_template}

[テンプレート ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン icon")](https://console.bluemix.net/devops/create){: new_window} から継続的デリバリー・ツールチェーンを作成して構成するには、以下のようにします。

1. **「ツールチェーンの作成 (Create a Toolchain)」**ページで、ツールチェーン・テンプレートをクリックします。
1. 作成しようとしているツールチェーンの図を確認します。この図は、ツールチェーン内の各ツール統合とそのライフサイクル・フェーズを示しています。

 **ヒント**: 一部のツールチェーン・テンプレートには、同じツール統合の複数のインスタンスが含まれています。例えば、{{site.data.keyword.Bluemix_notm}} Public の Microservices ツールチェーン・テンプレートには、GitHub の 3 つのインスタンスと Delivery Pipeline の 3 つのインスタンス (3 つのマイクロサービスのそれぞれに対して 1 つずつ) が含まれています。

 次のイメージの図はその例です。ツールチェーンを作成すると、ツールチェーンを構成する各ツール統合がこの図に表示されます。![ツールチェーンの図](images/toolchain_diagram.png)
1. ツールチェーン設定のデフォルト情報を確認します。ツールチェーンの名前は、そのツールチェーンを {{site.data.keyword.Bluemix_notm}} 内で識別するためのものです。別の名前を使用する場合は、ツールチェーンの名前を変更します。
1. 「ツール統合 (Tool Integrations)」セクションで、ツールチェーンに構成する各ツール統合を選択します。いくつかのツール統合は、構成を必要としません。ツール統合の構成については、[ツール統合の構成](/docs/services/ContinuousDelivery/toolchains_integrations.html){: new_window}を参照してください。
1. **「作成」**をクリックします。以下のようにいくつかのステップが自動的に実行されて、ツールチェーンがセットアップされます。セットアップされるツール統合は、どのツールチェーン・テンプレートを選択したのか、また、{{site.data.keyword.Bluemix_notm}} Public と {{site.data.keyword.Bluemix_notm}} Dedicated のどちらを使用しているのかによって異なります。例えば、Microservices ツールチェーンを {{site.data.keyword.Bluemix_notm}} Public で作成する場合、以下のステップが実行されます。

 * ツールチェーンが作成されます。
 * Delivery Pipeline を構成した場合は、パイプラインが作成されて実行します。
 * Sauce Labs を構成した場合は、パイプラインに Sauce Labs テスト・ジョブを追加するようにツールチェーンがセットアップされます。
 * PagerDuty を構成した場合は、指定した PagerDuty サービスにアラート通知を送信するようにツールチェーンがセットアップされます。
 * Slack を構成した場合は、指定した Slack チャネルにデプロイメント状況に関する通知を送信するようにツールチェーンがセットアップされます。
 * GitHub などのソース・コード・ツール統合を構成した場合、サンプル GitHub リポジトリーが GitHub アカウントに複製されます。
