# grails-fields-custom-widgets-and-wrappers

Sample app for the [grails-fields-custom-widgets-and-wrappers v8 guide][guide] on the Apache Grails site.

The guide walks through driving every CRUD page with `<f:all>`, `<f:display>`, and `<f:table>` from the Grails Fields plugin, then progressively customises wrappers, widgets, and table templates so per-property formatting concerns live once under `grails-app/views/_fields/` instead of scattered across every domain class's GSPs. It also covers the thinly-documented association widget intersection (`manyToOne`, `oneToOne`, `oneToMany`, `manyToMany`).

## Layout

| Directory | What it is |
|---|---|
| [`initial/`](initial/) | Vanilla Grails 8 snapshot starter (`web` profile, Hibernate, Tomcat, DevTools, JDK 25). Generated from `https://prev-snapshot.grails.org/create/web/example.library?gorm=HIBERNATE&servlet=TOMCAT&reloading=DEVTOOLS&javaVersion=JDK_25`. No customisations. |
| [`complete/`](complete/) | The same starter with every customisation from the guide applied: `Author`, `Book`, `ContactInfo`, `Tag` domain classes; `BookController` / `AuthorController` with `static scaffold`; replacement CRUD GSPs that use `<f:all>`, `<f:display>`, `<f:table>`; and all `_fields/` widget, wrapper, and table overrides. |

## Running

```bash
cd complete
./gradlew bootRun
```

Then browse to <http://localhost:8080/book/index> or <http://localhost:8080/author/index>.

## Branches

| Branch | Grails version |
|---|---|
| `grails8` | Apache Grails 8 (snapshot) |

## License

Apache License 2.0. See [LICENSE](LICENSE).

[guide]: https://grails.apache.org/guides/grails-fields-custom-widgets-and-wrappers/8/guide/index.html
