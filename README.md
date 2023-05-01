# The-12th-Gwangsan-gu-21-administrative-districts-data-analysis-and-convenience-store-location
After collecting and processing 159 cases of public data, the location conditions are analyzed and the optimal location for convenience stores is identified. Programmed in c++ Qt.

execution | map
:-: | :-:
<video src='https://user-images.githubusercontent.com/115389450/235430805-06e083ed-dceb-4af5-b349-d09902687312.mp4' width=180/> | <video src='https://user-images.githubusercontent.com/115389450/235430730-2cb6e8ec-7f9f-4d79-980c-53550eef6194.mp4' width=180/></video>

test
:-: 
<video src='https://user-images.githubusercontent.com/115389450/235430909-3ff207f3-2a5a-4872-83d6-75d401f64ca0.mp4' width=180/> </video>

![image](https://user-images.githubusercontent.com/115389450/235430301-6eb9ae24-336e-46ae-8c87-f27450c22337.png)
![image](https://user-images.githubusercontent.com/115389450/235430336-7c3a5fe3-920c-4a5b-849b-adc52066dabd.png)
![image](https://user-images.githubusercontent.com/115389450/235430367-1e6721db-96ca-4109-ae66-46f170fac088.png)

![image](https://user-images.githubusercontent.com/115389450/235428901-ae99eeed-4727-42d9-bcd1-5b01142d04a3.png)
![image](https://user-images.githubusercontent.com/115389450/235428980-80c59a1e-3cb6-4b49-ba2e-96d04b35dac7.png)
![image](https://user-images.githubusercontent.com/115389450/235429004-fc14cc49-86d3-471e-b668-b22fcce0be8c.png)
![image](https://user-images.githubusercontent.com/115389450/235429039-d0d3aa11-e1da-47d4-8d48-9d8571efffc7.png)
![image](https://user-images.githubusercontent.com/115389450/235429134-aade6b01-dd09-4eeb-ad37-3a23f196dddd.png)
![image](https://user-images.githubusercontent.com/115389450/235429207-9a56fc50-8c25-4d1d-b03d-af98c809ca00.png)
```
import pandas as pd



ref = pd.read_csv("인구수.csv")
print(ref)
ref2 = pd.read_csv("외국인구수정중.csv")
print(ref2)
ref3 = pd.merge(ref, ref2)
# ref3 = ref.join(ref2, how='outer', lsuffix='_caller', rsuffix='_other')
print(ref3)
# ref2 = ref.drop(["데이터기준일자"], axis=1)
ref3.to_csv("가공중2.csv", index=False)
# print(ref2)
# path_file = r'C:\Users\Kiot\AppData\Roaming\Python\Python39\site-packages\pandas'
# fn = 'population_gwangju.xlsx'
```
![image](https://user-images.githubusercontent.com/115389450/235429293-394e4de3-5550-45c4-9c1d-396f09222096.png)
![image](https://user-images.githubusercontent.com/115389450/235429332-db87fecc-712b-4ae6-a8fa-e978c2572596.png)
![image](https://user-images.githubusercontent.com/115389450/235429439-babbb083-01a2-4eb2-876f-ecec231429e7.png)
![image](https://user-images.githubusercontent.com/115389450/235429497-9b771ed8-1149-4771-8c77-dc1d9719062a.png)
![image](https://user-images.githubusercontent.com/115389450/235429550-02d4d1a8-d106-449d-a56b-e457d1fcdcb0.png)
![image](https://user-images.githubusercontent.com/115389450/235429593-b4c05fbf-f1af-4423-824b-bb4314625863.png)
![image](https://user-images.githubusercontent.com/115389450/235429622-5c2f6a77-51ba-401e-96f8-5210c434262e.png)
![image](https://user-images.githubusercontent.com/115389450/235429660-04e5c159-160b-41e8-970c-450e7aed5d90.png)
![image](https://user-images.githubusercontent.com/115389450/235429713-43630628-87d5-4320-acaf-3e48dca225e6.png)
![image](https://user-images.githubusercontent.com/115389450/235429744-5b0e210e-78b7-4875-bd03-8a2c81a013e3.png)
![image](https://user-images.githubusercontent.com/115389450/235429787-13e25460-380d-42b2-b4ee-fb354e2e4185.png)
![image](https://user-images.githubusercontent.com/115389450/235429840-d6e9e700-0304-45d6-9a0a-6b5ab82c1207.png)
# QML 코드
```
/****************************************************************************
**
** Copyright (C) 2019-2022 Klarälvdalens Datakonsult AB, a KDAB Group company, info@kdab.com
** Copyright (C) 2019-2022 General Magic B.V., info@generalmagic.com
**
** BSD License Usage
**
** Redistribution and use in source and binary forms, with or without
** modification, are permitted provided that the following conditions are
** met:
**   * Redistributions of source code must retain the above copyright
**     notice, this list of conditions and the following disclaimer.
**   * Redistributions in binary form must reproduce the above copyright
**     notice, this list of conditions and the following disclaimer in
**     the documentation and/or other materials provided with the
**     distribution.
**   * Neither the name of Klarälvdalens Datakonsult AB nor the names of
**     its contributors may be used to endorse or promote products derived
**     from this software without specific prior written permission.
**
**
** THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
** "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
** LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
** A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
** OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
** SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
** LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
** DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
** THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
** (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
** OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE."
****************************************************************************/

import QtQuick 2.12
import QtQuick.Controls 2.12
import QtQuick.Layouts 1.12
//! [SearchService plumbing]
import QtQuick.Window 2.12
import GeneralMagic 2.0
//import "./src"

Window {
    visible: true
    width: 900
    height: 700
    title: qsTr("선택지역 500m반경이내 건물 확인")
    property var updater: ServicesManager.contentUpdater(ContentItem.Type.RoadMap)
    Component.onCompleted: {
        //! [Set token safely]
        ServicesManager.settings.token = __my_secret_token;
        //! [Set token safely]

        ServicesManager.settings.allowInternetConnection = true; // enable connection to online services
        updater.autoApplyWhenReady = true;
        updater.update();
    }
//! [SearchService plumbing]

    //! [SearchService timer]
    Timer {
        id: searchTimer
        interval: 500
        onTriggered: {
            searchService.searchNow();
        }
    }
    //! [SearchService timer]

    //! [SearchService model]

    SearchService {
        id: searchService
        filter: searchBar.text
        searchMapPOIs: true
        searchAddresses: true
        limit: 10
//        thresholdDistance: 500 // 추가한 것. 지오코딩

        function searchNow() {
            searchTimer.stop();
            cancel();
            referencePoint = mapView.cursorWgsPosition();
            search();
        }
    }
    //! [SearchService model]

    MapView {
        id: mapView
        anchors.fill: parent
        gesturesEnabled: true
        onCursorPositionChanged: reverseGeocoding.reverseGeocode(mapView.cursorWgsPosition());
        Component.onCompleted: mapView.centerOnCoordinates(ServicesManager.createCoordinates(35.1580376, 126.79573574), 67);

//        RowLayout {
//            anchors.fill: parent
//            Rectangle {
//                Layout.fillWidth: true
//                Layout.fillHeight: true
//                color: "green"
////                anchors.topMargin: 15 // 바꾸고있음.
////                anchors.leftMargin: 15
////                anchors.rightMargin: 15
////                anchors.bottomMargin: 30
//                anchors.margins: 30
//            }
//        }

        ColumnLayout {
            anchors.fill: parent
            anchors.topMargin: 15 // 바꾸고있음.
            anchors.leftMargin: 15
            anchors.rightMargin: 15
            anchors.bottomMargin: 30

            //! [SearchService input]
            TextField {
                id: searchBar
                Layout.fillWidth: true
                placeholderText: qsTr("찾으려는 지역을 입력 해주세요.")
                onTextChanged: searchTimer.restart()
                onEditingFinished: searchService.searchNow()
            }
            //! [SearchService input]

            Rectangle {
                Layout.fillHeight: true
                Layout.fillWidth: true
                color: Qt.rgba(0,0,0,0.5)
                visible: searchBar.focus
                //! [SearchService list]
                ListView {
                    id: searchList
                    anchors.fill: parent
                    clip: true
                    model: searchService
                    functi
function distance(meters)
                    {
                        return meters >= 1000 ? (meters / 1000.).toFixed(3) + " Km" :  meters.toFixed(0) + " m";
                    }
                    delegate: Item {
                        height: row.height
                        RowLayout {
                            id: row
                            IconView {
                                iconSource: landmark.icon
                                Layout.maximumHeight: row.height
                                Layout.maximumWidth: row.height
                                width: height
                                height: row.height
                            }
                            ColumnLayout {
                                Layout.fillHeight: true
                                Layout.fillWidth: true
                                Text {
                                    Layout.fillWidth: true
                                    text: landmark.name + " (" + searchList.distance(landmark.coordinates.distance(searchService.referencePoint)) + ")"
                                    color: "white"
                                    font.pixelSize: 16
                                    wrapMode: Text.WrapAnywhere
                                }
                                Text {
                                    Layout.fillWidth: true
                                    text: landmark.description
                                    color: "white"
                                    font.pixelSize: 14
                                    font.italic: true
                                    wrapMode: Text.WrapAnywhere
                                }
                            }
                        }
                        MouseArea {
                            anchors.fill: row
                            onClicked: {
                                mapView.centerOnCoordinates(searchService.get(index).coordinates, -1);
                                searchBar.focus = true;
                            }
                        }
                    }
                }
                //! [SearchService list]
            }
            SearchService {
                id: reverseGeocoding
                searchMapPOIs: true
                searchAddresses: true
                limit: 10
                thresholdDistance: 500
            }
            Item {
//                Layout.fillHeight: true
//                Layout.fillWidth: true
                width : 400
                height : 400
//                Rectangle{
//                    anchors.fill: parent
//                    Layout.fillHeight: true
//                    Layout.fillWidth: true
//                    color: "green"
//                    anchors.margins: 30

                ListView {
                    id: searches
                    anchors.fill: parent
                    anchors.margins: 15
                    clip: true
                    model : reverseGeocoding
                    function distance(meters)
                    {
                        return meters >= 1000? (meters / 1000.).toFixed(3) + " Km" : meters.toFixed(0) + " m";
                    }
                    delegate: Item {
                        height : rows.height
                        RowLayout {
                            id : rows
                            IconView {
                                iconSource: landmark.icon
                                Layout.maximumHeight: rows.height
                                Layout.maximumWidth: rows.height
                                width : height
                                height : rows.height
                            }
                            ColumnLayout {
                                Layout.fillHeight: true
                                Layout.fillWidth: true
                                Text {
                                    Layout.fillWidth: true
                                    text : landmark.name + " (" + searchList.distance(landmark.coordinates.distance(reverseGeocoding.coordinates)) + ")"
                                    color : "black"
                                    font.pixelSize: 16
                                    wrapMode: Text.WrapAnywhere
                                }
                                Text {
                                    Layout.fillWidth: true
                                    text : landmark.description
                                    color : "black"
                                    font.pixelSize: 14
                                    font.italic: true
                                    wrapMode: Text.WrapAnywhere
                                }
                            }
                        }
                    }
//                }

//                    Revers{

//                    }
                }
            }
            RowLayout {    
 RowLayout {
                Button {
                    enabled: searchService.length
                    text: "선택지역 지도확대"
                    onClicked:  {
                        if (mapView.zoomLevel < 65)
                            mapView.zoomLevel = 65;
                        mapView.highlightLandmarkList(searchService)
                    }
                }
                Button {
                    text: "검색목록 업데이트"
                    onClicked: mapView.hideHighlights()
                }
            }
        }
    }
}
```
## 메인 CPP 소스
```
/****************************************************************************
**
** Copyright (C) 2019-2022 Klarälvdalens Datakonsult AB, a KDAB Group company, info@kdab.com
** Copyright (C) 2019-2022 General Magic B.V., info@generalmagic.com
**
** BSD License Usage
**
** Redistribution and use in source and binary forms, with or without
** modification, are permitted provided that the following conditions are
** met:
**   * Redistributions of source code must retain the above copyright
**     notice, this list of conditions and the following disclaimer.
**   * Redistributions in binary form must reproduce the above copyright
**     notice, this list of conditions and the following disclaimer in
**     the documentation and/or other materials provided with the
**     distribution.
**   * Neither the name of Klarälvdalens Datakonsult AB nor the names of
**     its contributors may be used to endorse or promote products derived
**     from this software without specific prior written permission.
**
**
** THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
** "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
** LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
** A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
** OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
** SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
** LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
** DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
** THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
** (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
** OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE."
****************************************************************************/

#include <QGuiApplication>
#include <QQmlApplicationEngine>
#include <QQmlContext>
#include <QQuickWindow>

int main(int argc, char *argv[])
{
    QCoreApplication::setAttribute(Qt::AA_EnableHighDpiScaling);

    QGuiApplication app(argc, argv);

#if QT_VERSION >= 0x060000
    QQuickWindow::setGraphicsApi(QSGRendererInterface::GraphicsApi::OpenGLRhi);
#else
    QQuickWindow::setSceneGraphBackend(QSGRendererInterface::GraphicsApi::OpenGL);
#endif

    QQmlApplicationEngine engine;
    const QUrl url(QStringLiteral("qrc:/main.qml"));
    QObject::connect(&engine, &QQmlApplicationEngine::objectCreated,
                     &app, [url](QObject *obj, const QUrl &objUrl) {
        if (!obj && url == objUrl)
            QCoreApplication::exit(-1);
    }, Qt::QueuedConnection);

    //! [Set token safely]
    // go to https://developer.generalmagic.com to get your token
    engine.rootContext()->setContextProperty("__my_secret_token", "eyJhbGciOiJFUzI1NiIsInR5cCI6IkpXVCJ9.eyJhdWQiOiI5ZTVmMjA5MS01NjFmLTRkNzQtOWQyMi1mZGVmNWExOTU4MmEiLCJleHAiOjE2NzkwMDQwMDAsImlzcyI6IkdlbmVyYWwgTWFnaWMiLCJqdGkiOiI1YjY0OWQ2Yi0wMjk4LTQwMjgtYWJjZC04ZDk3YmRiYzFhOTYiLCJuYmYiOjE2Nzg0MzEwOTZ9.KDlMchkap754Pu3ef19V-BUW2bwjS8G8vIzqmgpXfxWkmmC5xwJDep5-n70CXi7InZMwL2VdwkJZdok14XKcoQ" /*YOUR_TOKEN*/);
    // alternatively you can use :
    // qputenv("GEM_TOKEN", "your token");
    //! [Set token safely]

    engine.load(url);

    return app.exec();
}
```
## .pro 파일
```
#############################################################################
##
## Copyright (C) 2019-2022 Klarälvdalens Datakonsult AB, a KDAB Group company
## Copyright (C) 2019-2022 General Magic B.V.
## Contact: info@kdab.com, info@generalmagic.com
##
##
## BSD License Usage
##
## Redistribution and use in source and binary forms, with or without
## modification, are permitted provided that the following conditions are
## met:
##   * Redistributions of source code must retain the above copyright
##     notice, this list of conditions and the following disclaimer.
##   * Redistributions in binary form must reproduce the above copyright
##     notice, this list of conditions and the following disclaimer in
##     the documentation and/or other materials provided with the
##     distribution.
##   * Neither the name of Klarälvdalens Datakonsult AB nor the names of
##     its contributors may be used to endorse or promote products derived
##     from this software without specific prior written permission.
##
##
## THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
## "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
## LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
## A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT
## OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
## SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
## LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
## DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
## THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
## (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
## OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE."
#############################################################################

TEMPLATE = app

QT += qml quick

CONFIG += c++11

# The following define makes your compiler emit warnings if you use
# any Qt feature that has been marked deprecated (the exact warnings
# depend on your compiler). Refer to the documentation for the
# deprecated API to know how to port your code away from it.
DEFINES += QT_DEPRECATED_WARNINGS

# You can also make your code fail to compile if it uses deprecated APIs.
# In order to do so, uncomment the following line.
# You can also select to disable deprecated APIs only up to a certain version of Qt.
#DEFINES += QT_DISABLE_DEPRECATED_BEFORE=0x060000    # disables all the APIs deprecated before Qt 6.0.0

#QMAKE_DOCS = $$PWD/doc/general_magic_sdk_example.qdocconf

#HEADERS += \

SOURCES += \
        main.cpp

RESOURCES += qml.qrc

OTHER_FILES += \
            main.qml

# Additional import path used to resolve QML modules in Qt Creator's code model
QML_IMPORT_PATH =

# Additional import path used to resolve QML modules just for Qt Quick Designer
QML_DESIGNER_IMPORT_PATH =

# Default rules for deployment.
target.path = $$[QT_INSTALL_EXAMPLES]/GeneralMagic/FreeTextSearch
INSTALLS += target

ios {
    device: QMAKE_IOS_DEVICE_ARCHS = arm64
    QMAKE_IOS_DEPLOYMENT_TARGET = 9.0 #need support for thread-local
    CONFIG -= bitcode
    LIBS += -framework SystemConfiguration
}

android: include($$PWD/../3rdparty/android_openssl/openssl.pri)
```
