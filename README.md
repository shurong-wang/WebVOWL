### 数据加载 ###

* >> app.initialize

* >> ontologyMenu.setup

* >> setupUriListener

* >> parseUrlAndLoadOntology

* >> loadOntologyFromUri

* >> loadOntologyFromText

### 数据结构 ###

#### 顶层数据结构 #### 

```json
{
  "_comment": "",
  "header": {},
  "namespace": [],
  "metrics": {},
  "class": [],
  "classAttribute": [],
  "property": [],
  "propertyAttribute": []
}
```

#### class 结构 #### 

```json
[
    {
      "id": "4",
      "type": "owl:Class"
    },
    {
      "id": "5",
      "type": "owl:Class"
    }
]
```

#### classAttribute 结构 #### 

```json
[
    {
      "id": "4",
      "iri": "http://purl.org/muto/core#Tag",
      "baseIri": "http://purl.org/muto/core",
      "instances": 0,
      "annotations": {
        "isDefinedBy": [
          {
            "identifier": "是否被定义",
            "language": "cn",
            "value": "http://purl.org/muto/core#",
            "type": "iri"
          },
          {
            "identifier": "isDefinedBy",
            "language": "en",
            "value": "http://purl.org/muto/core#",
            "type": "iri"
          }
        ],
        "versionInfo": [
          {
            "identifier": "版本信息",
            "language": "cn",
            "value": "版本1.0:owl:为了使MUTO与owl Lite保持一致而删除了声明(声明在本例中不是必需的)。",
            "type": "label"
          },
          {
            "identifier": "versionInfo",
            "language": "en",
            "value": "Version 1.0: The owl:disjointWith statement was removed to make MUTO conform to OWL Lite (the statement is not essential in this case).",
            "type": "label"
          }
        ]
      },
      "label": {
        "IRI-based": "Tag",
        "cn": "标签",
        "en": "Tag"
      },
      "subClasses": [
        "6"
      ],
      "comment": {
        "cn": "标签由一个任意的文本标签组成。注意，在本体中没有合并相同标签的标记。",
        "en": "A Tag consists of an arbitrary text label. Note that tags with the same label are NOT merged in the ontology."
      },
      "superClasses": [
        "5"
      ]
    },
    {
      "id": "5",
      "iri": "http://www.w3.org/2004/02/skos/core#Concept",
      "baseIri": "http://www.w3.org/2004/02/skos/core",
      "instances": 0,
      "label": {
        "IRI-based": "Concept",
        "cn": "概念",
        "en": "Concept"
      },
      "subClasses": [
        "4"
      ],
      "attributes": [
        "external"
      ]
    }
]
```

#### property 结构 #### 

```json
[
    {
      "id": "0",
      "type": "owl:objectProperty"
    },
    {
      "id": "8",
      "type": "owl:datatypeProperty"
    },
]
```

#### propertyAttribute 结构 #### 

```json
[
    {
      "id": "0",
      "iri": "http://purl.org/muto/core#taggedResource",
      "baseIri": "http://purl.org/muto/core",
      "range": "2",
      "annotations": {
        "isDefinedBy": [
          {
            "identifier": "isDefinedBy",
            "language": "en",
            "value": "http://purl.org/muto/core#",
            "type": "iri"
          }
        ]
      },
      "label": {
        "IRI-based": "taggedResource",
        "cn": "已标记的资源",
        "en": "tagged resource"
      },
      "superproperty": [
        "3"
      ],
      "domain": "1",
      "comment": {
        "cn": "每个标记都链接到一个资源。这可以是任何类型的资源(例如，rdfs的所有子类:资源)，包括标记和标记。",
        "en": "Every tagging is linked to exactly one resource. This can be any kind of resource (i.e. all subclasses of rdfs:Resource), including tags and taggings."
      },
      "attributes": [
        "functional",
        "object"
      ]
    },
    {
      "id": "8",
      "iri": "http://purl.org/dc/terms/modified",
      "baseIri": "http://purl.org/dc/terms",
      "range": "10",
      "label": {
        "IRI-based": "modified"
      },
      "domain": "9",
      "attributes": [
        "datatype",
        "external"
      ]
    }
]
```


### 开发依赖 ###

* connect-livereload              //  
* copy-webpack-plugin             //  
* css-loader                      //  
* extract-text-webpack-plugin     //  
* grunt                           //  
* grunt-bump                      //  
* grunt-contrib-clean             //  
* grunt-contrib-compress          //  
* grunt-contrib-connect           //  
* grunt-contrib-copy              //  
* grunt-contrib-jshint            //  
* grunt-contrib-watch             //  
* grunt-gitinfo                   //  
* grunt-html-build                //  
* grunt-karma                     //  
* grunt-replace                   //  
* grunt-webpack                   //  
* jasmine-core                    //  
* karma                           //  
* karma-commonjs                  //  
* karma-jasmine                   //  
* karma-phantomjs-launcher        //  
* karma-spec-reporter             //  
* karma-webpack                   //  
* load-grunt-tasks                //  
* phantomjs-prebuilt              //  
* serve-favicon                   //  
* serve-static                    //  
* style-loader                    //  
* webpack                         //  
* webpack-dev-server              //  
