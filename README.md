# kopdar-41
Yuk Belajar Membuat Mobile Apps Dengan React Native 

-- App.js

[link Untuk Code](https://snack.expo.io/r18IySr7U)

#code

        import * as React from 'react';
        import { Image, Text, TextInput, View, TouchableOpacity, StyleSheet } from 'react-native';
        import Constants from 'expo-constants';

        // or any pure javascript modules available in npm
        import { Card } from 'react-native-paper';

        export default class extends React.Component {
          angkaDiClass = 50

          state= {
            iniTxt: "",
            topBarColor: "green"
          }
          render() {
            return (
               <View
                 style = {{
                   flex: 1,
                 }}
               >

                    <View style={{
                      backgroundColor: this.state.topBarColor,
                      justifyContent: "center",
                      alignItems: "center",
                      height: 60,
                      padding: 20
                    }}
                    >

                      <Text style={{
                       color: "white",
                       fontSize: 20,
                       fontWeight: "bold", 
                      }}>
                        Programmer Semarang
                      </Text>

                    </View>


                    <TouchableOpacity 
                    onPress= {() => {
                      this.fungsiGantiWarna()
                    }}

                    style={{
                      borderRadius: 10,
                      alignItems: "center",
                      justifyContent: "center",
                      height:40,
                      width:100,
                      backgroundColor: "crimson",
                    }}>
                      Button
                    </TouchableOpacity>

                    <Image 
                      source = {{uri: "https://helpx.adobe.com/content/dam/help/en/stock/how-to/visual-reverse-image-search/jcr_content/main-pars/image/visual-reverse-image-search-v2_intro.jpg"}}
                      style= {{ height: 200
                       }} 
                    />

                      <Image 
                      source = { require("./assets/snack-icon.png") }
                      style= {{ height: 200
                       }} 
                    />

                    <TextInput
                      multiline
                      onChangeText = {(value) => { this.setState({iniTxt: value})
                      }}
                      placeHolder= "ini apa"
                      style= {{
                      borderWidth: 2,
                      height: 50
                    }}/>

                    <TouchableOpacity
                      activeOpacity={0.8}
                      style= {{
                        alignItems: "center",
                        backgroundColor: "rgb(255,240, 50)",

                      }}
                    >
                      <Text
                        style={{ color: "white",
                        fontSize: 30,
                        }}>
                             Masuk Gan
                      </Text>
                    </TouchableOpacity>

                </View>
            );
          }

          fungsiAlert() {

            //let angka = 30

            //angka += 30
            this.angkaDiClass += 50
            alert(this.angkaDiClass.toString())
          }

          fungsiGantiWarna() {
            this.setState({
                topBarColor: "cyan"
            })
          }

          funsgiGantiTxt(){
            this.setState({

            })
          }

        }


