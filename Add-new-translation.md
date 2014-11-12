[[HOME|Home]] > [[TERASOLOGY LAUNCHER DOCUMENTATION|Documentation]] > [[ADD NEW TRANSLATION|add-new-translation]]

Adding new languages to the launcher's portfolio or helping out with translating just single labels or messages is quite easy. We offer two ways of doing so:

1. Using our [Weblate](http://weblate.org) web interface at [translate.terasology.org](http://translate.terasology.org/) (**Recommended**)
2. Manually creating/editing of some text bundle files and one Java file.

We strongly encourage you to use the Weblate interface as it allows for easy review of new translations or suggested changes. 

# Using Weblate
Using the Weblate interface is really easy! For the start, you can just log-in with your GitHub Account. By doing so your changes and translations will be recognized correctly in the Git commits. 

All translations needed for **TerasologyLauncher** can be found in the corresponding Weblate project:
- **[Weblate/TerasologyLauncher](http://translate.terasology.org/projects/terasologylauncher/)**

There are two sub-projects, one for the *Labels* (all descriptive labels and button texts of the launcher's UI) and one for *Messages* (e.g. for the update dialog, warnings, and error messages). Those two sub-projects can be found under
- **[Weblate/TerasologyLauncher/Labels](http://translate.terasology.org/projects/terasologylauncher/labels/)** 
- **[Weblate/TerasologyLauncher/Messages](http://translate.terasology.org/projects/terasologylauncher/messages/)**

You can add any new language to the round-up via the web interface. Note that English is the launcher's default language and can thus only be modified using [manual translation](#Manual Translation). For more information on how to use Weblate see the official [Translators guide](http://weblate.readthedocs.org/en/weblate-1.9/user/index.html).

# Manual Translation
Suppose you have done a translation to German. The necessary steps would be:
  * copy [`LabelsBundle_en.properties`](https://github.com/MovingBlocks/TerasologyLauncher/blob/develop/src/main/resources/org/terasology/launcher/bundle/LabelsBundle_en.properties) to a new file `LabelsBundle_de.properties` in ` src/main/resources/org/terasology/launcher/bundle/`. Replace the language suffix with the appropriate one (see http://en.wikipedia.org/wiki/ISO_639-1). Translate everything to your target language. The property files need to be valid Java properties files (ISO 8859-1 character encoding). (see http://docs.oracle.com/javase/7/docs/api/java/util/Properties.html).
  * do the same for `MessageBundle_de.properties`
  * add a `settings_language_de=...` entry to each `LabelsBundle_*.properties` file for other languages. This is used to display the new translation in the settings. Put only the translated name of the language as value, e.g. `settings_language_de=German` in the `en` file. In the settings menu, the label will be automatically extended to `German (Deutsch)`. 
  * make the launcher aware that there is a new language: Modify [`src/main/java/org/terasology/launcher/util/Languages.java`](https://github.com/MovingBlocks/TerasologyLauncher/blob/develop/src/main/java/org/terasology/launcher/util/Languages.java) so that you create a new locale, add your language to the supported locales and select the settings label. 

To keep everything nice and clean we adivse you to use a **feature branch**:
  * `git checkout develop`
  * `git branch germanTranslation`
  * `git checkout germanTranslation`
  * Add/Change files
  * `git commit ....`
  * `git push`
  * Open pull request

If you want, feel free to add yourself to the README.md as a contributor.