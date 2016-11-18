# ngSurvey


## Question Types


### Einfachauswahl

```HTML

<md-card-content>
    <p class="md-headline">Beurteilen Sie Ihre Irgendwas</p>
    <div layout="row" layout-align="space-between center">
        <div flex="30">
            <p class="md-subhead" style="padding-top:12px;">Hungrig</p>
        </div>
        <div>
            <md-radio-group ng-model="result.VAR_NAME_1" layout="row" layout-align="space-between center">
                <md-radio-button value="1">Sehr schlecht</md-radio-button>
                <md-radio-button value="2">Banana </md-radio-button>
                <md-radio-button value="3">Mango</md-radio-button>
                <md-radio-button value="4">gaga</md-radio-button>
                <md-radio-button value="5">Sehr gut</md-radio-button>
            </md-radio-group>
        </div>
    </div>
    <md-divider></md-divider>
    <div layout="row" layout-align="space-between center">
        <div flex="30">
            <p class="md-subhead" style="padding-top:12px;">Some more Items</p>
        </div>
        <div>
            <md-radio-group ng-model="result.VAR_NAME_2" layout="row" layout-align="space-between center">
                <md-radio-button value="1">Sehr schlecht</md-radio-button>
                <md-radio-button value="2">Banana </md-radio-button>
                <md-radio-button value="3">Mango</md-radio-button>
                <md-radio-button value="4">gaga</md-radio-button>
                <md-radio-button value="5">Sehr gut</md-radio-button>
            </md-radio-group>
        </div>
    </div>
</md-card-content>


```



## Basic-Template



```HTML

<div>
    <md-content class="md-padding" layout="row" layout-wrap="" layout-align="center start">
        <div flex-gt-sm="65" layout="column">
            <div ng-if="!thankyou">
                <form name="surveyForm">
                    <md-card ng-init="result.survey_version = 'ng_survey_v1'">
                        <md-card-title>
                            <md-card-title-text>
                                <span class="md-display-1" style="color:#3F51B5">Titel</span>
                                <span class="md-subhead" style="color:#9E9E9E">Beschreibung.</span>
                            </md-card-title-text>
                        </md-card-title>
                        <md-divider></md-divider>
                        <md-card-content>
                            
                        <!-- Fragen hier einfügen-->

                        </md-card-content>
                        <md-divider></md-divider>
                        <md-card-actions ng-if="surveyForm.$valid" layout="row" layout-align="end center">
                            <md-button ng-click="saveresult()">Speichern</md-button>
                        </md-card-actions>
                    </md-card>
                </form>
            </div>
            <div ng-if="thankyou">
                <h1 show-xs show-sm hide-gt-sm class="md-display-2">Herzlichen Dank</h1>
                <h1 show-gt-sm hide-sm hide-xs class="md-display-4">Herzlichen Dank</h1>
                <span class="md-subhead" style="margin-top:-48px;">
                Ihre Eingabe wurde erfolgreich gespeichert! Sie können nun dieses Fenster schliessen.
                </span>
            </div>
        </div>
    </md-content>
</div>


```


