# Spring Boot


## Actions

- [GitHub Actionsのドキュメント - GitHub Docs](https://docs.github.com/ja/actions)

## packages を使う

pom.xmlに追加

```xml
	<distributionManagement>
		<repository>
			<id>github</id>
			<name>GitHub OWNER Apache Maven Packages</name>
			<url>https://maven.pkg.github.com/<AccountName>/actions-sb-demo</url>
		</repository>
	</distributionManagement>
```

Actions で `Publish Java Package with Maven` のワークフローを作成。
ActionsからはこれでPackagesに登録できる。

ローカルから直接mvn deployしたい場合は、wite:packages権限のあるトークンを生成して、~/.m2/settings.xmlに以下を追加

```xml
  <servers>
    <server>
      <id>github</id>
      <username>kuresato</username>
      <!-- personal access token -->
      <password>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</password>
    </server>
  </servers>
```


参考
- [MavenでGitHub PackagesへJARをデプロイする - Qiita](https://qiita.com/backpaper0@github/items/4d2d83a707b50b9f0151)

## JUnitレポート

- [JUnit Report Action · Actions · GitHub Marketplace](https://github.com/marketplace/actions/junit-report-action)
- [GitHub Actions でユニットテストの結果をレポートする - Speaker Deck](https://speakerdeck.com/hkusu/github-actions-deyunitutotesutofalsejie-guo-worepotosuru)

