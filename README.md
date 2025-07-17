// VATRITRA Mikaroka - App Pages (Landing, CV, Chat, Offers, Upload, Payment)

import React, { useState } from "react";

export default function HomePage() { const [page, setPage] = useState("home");

const renderPage = () => { switch (page) { case "cv": return <CVPage />; case "chat": return <ChatPage />; case "offers": return <JobOffersPage />; case "upload": return <UploadPage />; case "payment": return <PaymentPage />; default: return <LandingPage setPage={setPage} />; } };

return ( <div className="min-h-screen bg-white text-gray-800 dark:bg-zinc-900 dark:text-white"> <nav className="flex justify-center gap-4 p-4 bg-white dark:bg-zinc-800 shadow"> <button onClick={() => setPage("home")}>Home</button> <button onClick={() => setPage("cv")}>CV</button> <button onClick={() => setPage("chat")}>Chat</button> <button onClick={() => setPage("offers")}>Tolotra Asa</button> <button onClick={() => setPage("upload")}>Fandefasana Sary</button> <button onClick={() => setPage("payment")}>Fandefasana Vola</button> </nav> {renderPage()} </div> ); }

function LandingPage({ setPage }) { return ( <main className="flex flex-col items-center justify-center py-20 px-4 text-center"> <h2 className="text-3xl md:text-4xl font-semibold mb-4">Mitady Asa Ve Ianao?</h2> <p className="mb-6 text-lg">Sehatra ho an’ny mpitady sy mpampiasa asa</p> <div className="flex flex-col md:flex-row gap-4"> <button className="px-6 py-3 border-2 border-blue-800 text-blue-800 rounded-xl hover:bg-blue-50 dark:border-blue-300 dark:text-blue-300 dark:hover:bg-blue-800 dark:hover:text-white"> Miditra </button> <button className="px-6 py-3 bg-orange-400 text-white rounded-xl hover:bg-orange-500"> Misoratra anarana </button> </div> <button className="mt-6 px-6 py-3 bg-blue-800 text-white rounded-xl hover:bg-blue-900"> Hijery tolotra asa </button> </main> ); }

function CVPage() { return ( <section className="p-8"> <h2 className="text-2xl font-semibold mb-4">Kaonty & CV</h2> <p>Asehoy sy havaozy ny CV sy mombamomba anao eto.</p> </section> ); }

function ChatPage() { return ( <section className="p-8"> <h2 className="text-2xl font-semibold mb-4">Hafatra sy Fifandraisana</h2> <p>Mifandray amin'ny olona sy orinasa amin'ny alalan'ny chat eto.</p> </section> ); }

function JobOffersPage() { return ( <section className="p-8"> <h2 className="text-2xl font-semibold mb-4">Tolotra Asa</h2> <p>Hijery sy hitady asa eto amin'ny sehatra misy anao.</p> </section> ); }

function UploadPage() { return ( <section className="p-8"> <h2 className="text-2xl font-semibold mb-4">Fandefasana Sary</h2> <p>Mandefa sary na antontan-taratasy mifandray amin’ny asa eto.</p> </section> ); }

function PaymentPage() { return ( <section className="p-8"> <h2 className="text-2xl font-semibold mb-4">Fandefasana Vola</h2> <p>Manaova fandoavam-bola amin'ny alalan'ny rafitra azo antoka.</p> </section> ); }

