Complex Components

Single  Components

We could build this entire UI in a single component. However, building an entire application in a single component is not a great idea as it can grow huge, complex, and difficult to test.
---------------------------------------------------------------------

-Break it down by
	-The container component
	-Child components
-Put it all together

----------------------------------------------------------------------
example

class Timeline extends React.Component {
  render() {
    return (
      <div className="notificationsFrame">
        <div className="panel">
          <div className="header">

            <div className="menuIcon">
              <div className="dashTop"></div>
              <div className="dashBottom"></div>
              <div className="circle"></div>
            </div>

            <span className="title">Timeline</span>

            <input
              type="text"
              className="searchInput"
              placeholder="Search ..." />

            <div className="fa fa-search searchIcon"></div>
          </div>
          <div className="content">
            <div className="line"></div>
            <div className="item">

              <div className="avatar">
                <img
                alt='doug'
                src="http://www.croop.cl/UI/twitter/images/doug.jpg" />
              </div>

              <span className="time">
                An hour ago
              </span>
              <p>Ate lunch</p>
            </div>

          </div>
        </div>
      </div>
    )
  }
}

The container component

class Header extends React.Component {
  render() {
    return (
      <div className="header">

            <div className="menuIcon">
              <div className="dashTop"></div>
              <div className="dashBottom"></div>
              <div className="circle"></div>
            </div>

            <span className="title">Timeline</span>

            <input
              type="text"
              className="searchInput"
              placeholder="Search ..." />

            <div className="fa fa-search searchIcon"></div>
          </div>
    )
  }
}

Child component

class Content extends React.Component {
  render() {
    return (
      <div className="content">
            <div className="line"></div>
            <div className="item">

              <div className="avatar">
                <img
                alt='doug'
                src="http://www.croop.cl/UI/twitter/images/doug.jpg" />
              </div>

              <span className="time">
                An hour ago
              </span>
              <p>Ate lunch</p>
            </div>

          </div>
    )
  }
}

Put it all together

class App extends React.Component {
  render() {
    return (
      <div className="notificationsFrame">
        <div className="panel">
        	<Header/>
        	<Contnet/>
       </div>
      </div>
    )
  }
}

---------------------------------------------------------------------
Comments

{/* This is React comment*/}