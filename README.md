# 78



https://api.wheretheiss.at/v1/satellites/25544

--------------------------------------------

from google got the below one:


http://api.open-notify.org/iss-now.json

\


http://open-notify.org/Open-Notify-API/ISS-Location-Now/



\



  getLocation() {
    axios
      //.get('https://api.wheretheiss.at/v1/satellites/25544')
      .get("http://api.open-notify.org/iss-now.json")
      .then((res) => {
       // this.setState({ location: res.data });
       this.setState({location:res.data.responseJSON.iss_position})
        console.log(res.data.responseJSON.iss_position);
      })
      .catch((err) => {
        Alert.alert(err.message);
        console.error(err);
      });
  }
