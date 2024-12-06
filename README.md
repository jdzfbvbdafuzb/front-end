import React, {useState} from "react"; 
const useStateTask = () => {
const [color,setColor] = useState("");
  return (
    <div className={`flex space-x-4 w-full h-screen bg-${color}-800`}>
      <p>Change Color</p>
      <button className="border bg-red-800 py-4 px-6"
      onClick={() => {
        setColor("red");
      }}
      >
       red
      </button>
      <button className="border bg-blue-800 py-4 px-6"
      onClick={() => {
        setColor("blue");
      }}
      >
       blue
      </button>
      <button className="border bg-green-800 py-4 px-6"
      onClick={() => {
        setColor("green");
      }}
      >
       green
      </button> 
    </div>
  );
};

export default useStateTask;

import { useState} from "react"
export default function Task2(){
    const [search, setSearch] = useState("");

    console.log("search utga--->",search)
    return(
        <div className="flex-center justify h-screen flex-col">
            <input
            type="search"
            onChange={(test) => setSearch(test.target.value)}
            className="border-2 border-black rounded"        
            >
                <p>search: {search}</p>
            </input>
        </div>
    );
}



import { useState } from "react";

export default function Week3() {
  const [grid, setGrid] = useState(false);
  const data = [
    {
      id: 1,
      title: "Test",
      description:
        "orem ipsum dolor sit amet, consectetur adipiscing elit. Cras at est laoreet sem efficitur placerat. Nam in tincidunt tellus. Mauris placerat, ipsum vel accumsan mattis, tortor eros elementum neque, a luctus odio nisi sit amet nisl.",
    }, //0
    {
      id: 2,
      title: "Test",
      description:
        "orem ipsum dolor sit amet, consectetur adipiscing elit. Cras at est laoreet sem efficitur placerat. Nam in tincidunt tellus. Mauris placerat, ipsum vel accumsan mattis, tortor eros elementum neque, a luctus odio nisi sit amet nisl.",
    }, //1
    {
      id: 3,
      title: "Test3",
      description:
        "orem ipsum dolor sit amet, consectetur adipiscing elit. Cras at est laoreet sem efficitur placerat. Nam in tincidunt tellus. Mauris placerat, ipsum vel accumsan mattis, tortor eros elementum neque, a luctus odio nisi sit amet nisl.",
    }, //2
    {
      id: 4,
      title: "Test4",
      description:
        "orem ipsum dolor sit amet, consectetur adipiscing elit. Cras at est laoreet sem efficitur placerat. Nam in tincidunt tellus. Mauris placerat, ipsum vel accumsan mattis, tortor eros elementum neque, a luctus odio nisi sit amet nisl.",
    }, //3
    {
      id: 5,
      title: "Test5",
      description:
        "orem ipsum dolor sit amet, consectetur adipiscing elit. Cras at est laoreet sem efficitur placerat. Nam in tincidunt tellus. Mauris placerat, ipsum vel accumsan mattis, tortor eros elementum neque, a luctus odio nisi sit amet nisl.",
    }, //4
    {
      id: 6,
      title: "Test6",
      description:
        "orem ipsum dolor sit amet, consectetur adipiscing elit. Cras at est laoreet sem efficitur placerat. Nam in tincidunt tellus. Mauris placerat, ipsum vel accumsan mattis, tortor eros elementum neque, a luctus odio nisi sit amet nisl.",
    }, //5
  ];

  return (
    <div className="p-8 m-6 bg-white">
      <div className="flex items-center justify-between m-6">
        <h1 className="text-4xl text-black style-bold ">Нийтлэгүүд</h1>
        <button
          onClick={() => setGrid(!grid)}
          className="p-4 bg-blue-700 text-white rounded hover:bg-red-500 transition"
        >
          Grid View рүү шилжих {grid ? "list":"Grid"}
        </button>
      </div>
<div className="h-screen">
<div className={`${grid == true ? "grid grid-cols-2 gap-6" : ""}`}>
        {data.map((item) => (
          <div className={`space-y-4 border-2 mb-4 p-2 rounded hover:bg-slate-300 text-black `}>
            <p>{item.title}</p>
            <p>{item.description}</p>
          </div>
        ))}
      </div>
    </div>
</div>
      
  );
}
